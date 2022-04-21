---
title: "Elements"
description: "this is meta description"
draft: false
---


### Elements

This page demonstrate some basic elements and typography which you will use frequently within your site. Make the text **bold** or make it *italic*. Why not **_bold and italic_** both at a time. Here is the link to [Hugo](https://gohugo.io/) website. Do you want to link a long text [here how it looks in this theme](https://gohugo.io/).

URLs and URLs in angle brackets will automatically get turned into links. https://gohugo.io/ or <https://gohugo.io/> and sometimes example.com (but not on Github, for example).

# Heading one
## Heading two
### Heading three
#### Heading four
##### Heading five
###### Heading six

### Paragraph

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

<hr>

### Ordered List

1. The leap into electronic typesetting
2. It was popularised in the 1960s
3. Recently with desktop publishing software
4. An unknown printer took a galley
5. It has survived not only five centuries

<hr>

### Unordered List

* The leap into electronic typesetting
* It was popularised in the 1960s
* Recently with desktop publishing software
* An unknown printer took a galley
* It has survived not only five centuries

<hr>

### Blockquote

> Since its beginning in the 1950s, the field of artificial intelligence has cycled several times between periods of optimistic predictions and investment
<cite>Alexender Toto</cite>

<hr>

### Twitter Card

{{< tweet user="SanDiegoZoo" id="1453110110599868418" >}}

<hr>

### Code and Syntax Highlighting

Inline `code` has `back-ticks` around it.

#### HTML
```html
<article class="card post-card h-100 border-0 bg-transparent">
  <div class="card-body">
    <div class="post-image position-relative">
      <img class="w-100 h-auto rounded" src="/images/box.webp" alt="alter caption">
    </div>
    <a class="d-block" href="/blog/analysisi-ai-winter/" title="train is running out of steam">
      <h3 class="mb-3 post-title">The AGI hype train is running out of steam</h3>
    </a>
  </div>
</article>
```
#### Javascript
```javascript
$(window).scroll(function () {
  if ($(window).scrollTop() >= 50) {
    $('.header-nav').addClass('header-sticky-top');
  } else {
    $('.header-nav').removeClass('header-sticky-top');
  }
});
```

<hr>

### Markdown table

Colons can be used to align columns.

| Firsname   |	Lastname  |	Age        |	Lives in   |	Profession | Hobby      |
| ---------- | ---------- |	---------- |	---------- |	---------- | ---------- |
| Jill       |	Smith     |	29         |	New york   |	Developer  | Soccer     |
| Eve        |	Jackson   |	36         |	New york   |	Musicial   | Karaoke    |

<hr>

### Responsive HTML table

<div class="table-responsive">
  <table class="table">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
        <th scope="col">Heading</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">1</th>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <th scope="row">2</th>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
      <tr>
        <th scope="row">3</th>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
        <td>Cell</td>
      </tr>
    </tbody>
  </table>
</div>

<hr>

### Image

{{< image src="images/blog/02.jpg" alt="image caption" title="this is example title" caption="This is example photo caption">}}

<hr>

### Gallery
<div class="gallery">
{{< image src="images/blog/01.jpg" alt="image caption" title="this is example title">}}
{{< image src="images/blog/02.jpg" alt="image caption" title="this is example title">}}
{{< image src="images/blog/03.jpg" alt="image caption" title="this is example title">}}
{{< image src="images/blog/04.jpg" alt="image caption" title="this is example title">}}
{{< image src="images/blog/05.jpg" alt="image caption" title="this is example title">}}
{{< image src="images/blog/06.jpg" alt="image caption" title="this is example title">}}
</div>

<hr>

### Youtube video

{{< youtube NC0WPQd_bds >}}

<hr>

### Vimeo video

{{< vimeo 341490793 >}}