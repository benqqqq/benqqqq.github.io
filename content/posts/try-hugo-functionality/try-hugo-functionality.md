---
title: "Try Hugo Functionality"
date: 2023-05-24T16:09:17+08:00
showToc: true
tocOpen: true
tags: ['Hugo', 'Demo']
Description: 'Demo each cool functions / tips'
Summary: 'Demo each cool functions / tips'
---


### ✨ Hugo Built-in 

#### 🔰 Shortcode list in GitHub source code 
https://github.com/gohugoio/hugo/tree/99407c39ba92b3bfc569a505b05033e04b242e8d/tpl/tplimpl/embedded/templates/shortcodes
Find parameter here


#### 🔰 Figure 
https://gohugo.io/content-management/shortcodes/#figure
{{< figure 
    src="../let-me-do-it-for-you.png" 
    title="let me do it for you"
    link="https://gohugo.io/content-management/shortcodes/#figure"
>}}

```md
{{</* figure 
    src="../let-me-do-it-for-you.png" 
    title="let me do it for you"
    link="https://gohugo.io/content-management/shortcodes/#figure"
*/>}}
```


#### 🔰 Escape shortcode
https://liatas.com/posts/escaping-hugo-shortcodes/

add `/*`
```md
{{</*/*
    code you need to be escaped
*/*/>}}
```


#### 🔰 param
https://gohugo.io/content-management/shortcodes/#param

{{< param title >}}
```md
{{</* param title */>}}
```

#### 🔰 Youtube
https://gohugo.io/content-management/shortcodes/#youtube

{{< youtube XCqLuEAmNW8 >}}
```md
{{</* youtube XCqLuEAmNW8 */>}}
```


### 🎁 Supported by theme PaperMod 

#### 🔰Collapse
https://github.com/benqqqq/hugo-PaperMod/blob/8c2f997ab398ad57d49c04ffbb6474c64adf2ec7/layouts/shortcodes/collapse.html

{{< collapse summary="This is summary" >}}
 Hidden detail 
{{< /collapse >}}

```md
{{</* collapse summary="This is summary" */>}}
 Hidden detail 
{{</* /collapse */>}}
```