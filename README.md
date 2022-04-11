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
    |---year
        |---postTitle
            |---index.md
```

```bash
hugo new post/{{year}}/{{postTitle}}/index.md
```

```bash
hugo new post/{{year}}/{{postTitle}}.md
```

Blog icon attribution - https://pixabay.com/photos/hardware-electronics-repair-service-3509891/
Image by <a href="https://pixabay.com/users/marijana1-8558212/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3509891">marijana1</a> from <a href="https://pixabay.com/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3509891">Pixabay</a>

![blog](https://img.shields.io/website-up-down-green-red/https/cloud.fskelly.com.svg)  
![Publish Blog](https://github.com/fskelly/flkelly-cloudblog/actions/workflows/azure-static-web-apps-lively-field-0f34d4403.yml/badge.svg)  
![Website maintained](https://img.shields.io/maintenance/yes/2021?style=plastic)
