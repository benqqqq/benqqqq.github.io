---
title: "Managing Multiple Github Accounts From One Machine"
date: 2023-07-11T23:02:17+08:00
showToc: true
tocOpen: true
---


Think about this. You have two GitHub accounts, one for personal projects and another one for work. 
You want to clone repositories from both accounts onto the same machine. 
How do you manage them without conflict? 
That's what I'll share in this article: my way to configuring a system to handle multiple GitHub accounts.

But first, we need to understand the structure and workflow:

1. Setting up the directory structure.
2. Generating SSH keys for both accounts.
3. Generating GPG keys for both accounts.
4. Configuring `.gitconfig` files for both accounts.

With that overview in mind, let's get started!

### The Directory Structure
---

```bash
.
├── .ssh
│   ├── github-personal.pub
│   ├── github-personal
│   ├── github-work.pub
│   └── github-work
├── .gitconfig
└── repo
    ├── .gitconfig.personal
    ├── .gitconfig.work
    ├── personal
    │   └── some-personal-repo
    └── work
        └── some-work-repo
```

- With this directory structure, To clone the personal repository, 
simply navigate to `~/repo/personal`. 
For the work repository, navigate to `~/repo/work`.


### Generating SSH keys
---

- I generate SSH keys for both accounts using

```bash
ssh-keygen -t ed25519 -C "<work-email>" -f ~/.ssh/github-work
ssh-keygen -t ed25519 -C "<personal-email>" -f ~/.ssh/github-personal
```

- Then, get the public key of each ssh key pair using

```bash
tr -d '\n' < ~/.ssh/github-<work|personal>.pub | pbcopy
```

- Finally, I put each ssh public key into its respective GitHub account: GitHub → Settings → SSH and GPG keys → New SSH key.

### Generating GPG signatures
---

Here, I've installed gpg via Homebrew.

- Generate gpg key pair for each account:

```bash
gpg --full-generate-key 
```

- To get the `key id` and `fingerprint` for each account, use:

```bash
gpg --list-secret-keys  --keyid-format LONG                                                                               
```

Here is a sample output:

```markdown
------------
sec   rsa3072/<key id> 2023-07-11 [SC]
      <fingerprint>
uid                 [ultimate] Name <work email>
ssb   rsa3072/xxxxxxxxxxxx 2023-07-11 [E]
```

- Export the public key of gpg in armor format:

```bash
gpg --armor --export <fingerprint>
```

- Finally, put each corresponding GPG public key in GitHub: GitHub → Settings → SSH and GPG keys → New GPG key.

### Configuring `.gitconfig` Files
---

Here are how my `.gitconfig` files look like:

- In the main `~/.gitconfig` file:

```markdown
[gpg]
    program = /opt/homebrew/bin/gpg 
[includeIf "gitdir:~/repo/personal/"]
    path = ~/repo/.gitconfig.personal
[includeIf "gitdir:~/repo/work/"]
    path = ~/repo/.gitconfig.work
```

- In the `~/repo/.gitconfig.personal` file:

```markdown
[user]
  name = ...
 	email = ...
 	signingKey = <gpg key id>
[commit]
    gpgsign = true
[github]
    user = ...
[core]
    sshCommand = "ssh -i ~/.ssh/github-personal"
```

- In the `~/repo/.gitconfig.work` file:

```markdown
[user]
  name = ...
 	email = ...
 	signingKey = <gpg key id>
[commit]
    gpgsign = true
[github]
    user = ...
[core]
    sshCommand = "ssh -i ~/.ssh/github-work"
```

And that's it! This setup works for me!

*Notes: Why did I need to come up with this guide? Here are some reasons:*

- [How To Work With Multiple Github Accounts on a single Machine](https://gist.github.com/rahularity/86da20fe3858e6b311de068201d279e3): The proposed solution used different hostnames, which was inconvenient for my use case. Plus, it didn't cover using GPG signatures or doing gitconfig.

- [How to use multiple users with Git](https://dev.to/equiman/how-to-use-multiple-users-with-git-2e9l): This solved the gitconfig issue by using separate gitconfig files for each account, but again, it didn't mention how to handle SSH or GPG signatures.

- [8 Easy Steps to Set Up Multiple Git Accounts](https://blog.gitguardian.com/8-easy-steps-to-set-up-multiple-git-accounts/): This guide tackled SSH issues and used different gitconfig for each account, yet it didn't cover GPG signatures.

- [Github Documentation on GPG Keys](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key): This provides critical information about GPG keys but is not a holistic guide in itself.

- [Using git with multiple profiles and GPG+SSH keys](https://markentier.tech/posts/2021/02/github-with-multiple-profiles-gpg-ssh-keys/): Although this guide covered gitconfig, SSH key pairs and briefly mentioned GPG, it proposed the use of different hostnames, which didn't suit my needs.

So this is a complete guide with all solutions stitched together, tailored to meet my needs.
