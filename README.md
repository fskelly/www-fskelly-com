# Purpose

This is the backend for my Cloud based blog  
[Fletcher's Blog](https://www.fskelly.com)

My build command

```bash
C:\ProgramData\chocolatey\lib\hugo-extended\tools\hugo.exe
```

## Create a new post

I like to create my content based upon year  
My folder structure looks like this  

```bash
content  
|---post
    |---contentType
        |---year
            |---postTitle
                |---index.md
```

```bash
hugo new post/{{contentType}}/{{year}}/{{postTitle}}/index.md
```

For Example  

```bash
hugo new post/home-automation/2022/newPost/index.md
```

Blog icon attribution - <https://pixabay.com/photos/hardware-electronics-repair-service-3509891/>
Image by <a href="https://pixabay.com/users/marijana1-8558212/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3509891">marijana1</a> from <a href="https://pixabay.com/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3509891">Pixabay</a>

![blog](https://img.shields.io/website-up-down-green-red/https/www.fskelly.com.svg)  
![Publish Blog](https://github.com/fskelly/www-fskelly-com/actions/workflows/azure-static-web-apps-nice-cliff-05e0aea03.yml/badge.svg)  
![Website maintained](https://img.shields.io/maintenance/yes/2022?style=plastic)
