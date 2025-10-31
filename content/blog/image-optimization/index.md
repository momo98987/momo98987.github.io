---
title: " ILight Holographic Perception Smart Transportation Project"
comments: false
socialShare: true
toc: true
cover:
  src: ./alexandre-van-thuan-mr9FouttLGY-unsplash.jpg
  alt:
    The interior of Stadsbiblioteket in Stockholm - Gunnar Asplunds library from
    1928. The architecture is a transition between neoclassicism and
    functionalism.
  caption: By [Alexandre Van Thuan](https://unsplash.com/photos/mr9FouttLGY)
---

During my participation in the ILight Holographic Perception Smart Transportation Project, I was deeply involved in the entire process from technology R&D to practical implementation. With the core goal of "solving urban traffic pain points and building a new smart transportation ecosystem", the project integrates cutting-edge technologies to create a "cloud-edge-end" collaborative smart transportation solution. The details can be elaborated from two aspects: core functions and target tasks.

- Core Functions: Building a "Three Modules + One Platform"     Technical Closed Loop
- Target Tasks: From Technology Implementation to Value Realization

## PROJECTS

Use the [front matter](https://gohugo.io/content-management/front-matter/) of
your posts to add cover images:

<!-- markdownlint-disable MD013 -->

```markdown
---
cover:
  src: alexandre-van-thuan-mr9FouttLGY-unsplash.jpg
  alt:
    The interior of Stadsbiblioteket in Stockholm - Gunnar Asplunds library from
    1928. The architecture is a transition between neoclassicism and
    functionalism.
  caption: By [Alexandre Van Thuan](https://unsplash.com/photos/mr9FouttLGY)
---
```

<!-- markdownlint-enable MD013 -->

## Captions

Add captions to your inline images like this:

```markdown
---
![Alt text](image-url.jpg "Caption with **markdown support**")
---
```

![The main library in Vancouver is architecturally significant. The angles and levels contour together to produce a trippy scene. It's pretty from the outside but stunning from the inside.](aaron-thomas-dMqlE7lgyOU-unsplash.jpg "The main library in Vancouver is architecturally significant. The angles and levels contour together to produce a trippy scene. It's pretty from the outside but stunning from the inside. By [Aaron Thomas](https://unsplash.com/photos/dMqlE7lgyOU)")

## JPEG and WebP Quality

The default quality is 75%. See the
[official Image Processing Config Hugo docs](https://gohugo.io/content-management/image-processing/#image-processing-config).
Change it by adding the following to the `hugo.toml` file:

```toml
[imaging]
  quality = 75
```

## Resizing

By default, the theme creates resized versions of images ranging from 300 to 700
pixels wide in increments of 100 pixels. Override the resize behavior by adding
the following to the `hugo.toml` file:

```toml
[params]
  [params.imageResize]
    min = 300
    max = 700
    increment = 100
```

## Lazy Loading

Images are lazily loaded by default using the `loading="lazy"` attribute on HTML
`img` tags.

{{< video src="lazy-loading" autoplay="true" controls="false" loop="true" >}}
