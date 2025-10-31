---
title: "Backend & Data Practice: Solidifying the Technical Foundation"
comments: false
socialShare: true
toc: true
---

In backend development, I focus on building services with Java + SpringBoot as
the core. I participated in the microservice transformation of a course-based
e-commerce demo, integrating basic tools to resolve data consistency issues
between "orders and inventory," and optimized interface response time by 30%.
Meanwhile, I leverage the efficiency of Python: I crawled public industry data
using Python + Scrapy, and combined Pandas for data cleaning and Matplotlib for
visualization to provide data support for the "user behavior analysis" module in
course projects. Additionally, I completed a small embedded project with C language,
optimizing the communication protocol parsing logic of simple devices to deepen my
understanding of underlying technologies.

<!--more-->

Here is a an example configuration demonstrating how to configure `languages`
and `plugins` in the `hugo.toml` file of your Hugo site:

```toml
[params]
  [params.prism]
    languages = [
      "markup",
      "css",
      "clike",
      "javascript"
    ]
    plugins = [
      "normalize-whitespace",
      "toolbar",
      "copy-to-clipboard"
    ]
```

## Languages

The following languages are available:

<!-- markdownlint-disable MD033 -->
<pre class="language-none" style="max-height: 500px">
  <code>
    {{% prism-features "languages" %}}
  </code>
</pre>
<!-- markdownlint-enable MD033 -->

## Plugins

Before using a plugin in production, read its documentation and test it
thoroughly. E.g., the
[`remove-initial-line-feed` plugin](https://prismjs.com/plugins/remove-initial-line-feed/)
is still available despite being deprecated in favor of
[`normalize-whitespace`](https://prismjs.com/plugins/normalize-whitespace/).

Many Prism plugins require using `<pre>` tags with custom attributes. Hugo uses
Goldmark as Markdown handler, which by default doesn't render raw inline HTML,
so make sure to enable
[`unsafe`](https://gohugo.io/getting-started/configuration-markup#goldmark)
rendering if required:

```toml
[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true
```

The following plugins are available:

```none
{{% prism-features "plugins" %}}
```

### Examples

#### Copy to Clipboard

`copy-to-clipboard` requires the `toolbar` plugin, so make sure to add it
**after** adding `toolbar` in the `hugo.toml` file:

Config:

```toml
[params.prism]
  # ...
  plugins = [
    "toolbar",
    "copy-to-clipboard"
  ]
```

#### Line Numbers

Config:

```toml
[params.prism]
  plugins = [
    "line-numbers"
  ]
```

Input:

```html
<pre class="line-numbers">
  <code>
    Example
  </code>
</pre>
```

Output:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-none" data-start="42">
  <code>
    Hello,
    World!

    Foo
    Bar
  </code>
</pre>
<!-- markdownlint-enable MD033 -->

#### Command Line

Config:

```toml
[params.prism]
  languages = [
    "bash"
  ]
  plugins = [
    "command-line"
  ]
```

Input:

```html
<pre class="command-line language-bash" data-user="root" data-host="localhost">
  <code>
    cd /usr/local/etc
    cp php.ini php.ini.bak
    vi php.ini
  </code>
</pre>

<pre
  class="command-line language-bash"
  data-user="chris"
  data-host="remotehost"
  data-output="2, 4-8"
>
  <code>
    pwd
    /usr/home/chris/bin
    ls -la
    total 2
    drwxr-xr-x   2 chris  chris     11 Jan 10 16:48 .
    drwxr--r-x  45 chris  chris     92 Feb 14 11:10 ..
    -rwxr-xr-x   1 chris  chris    444 Aug 25  2013 backup
    -rwxr-xr-x   1 chris  chris    642 Jan 17 14:42 deploy
  </code>
</pre>
```

Output:

<!-- markdownlint-disable MD033 -->
<pre class="command-line language-bash" data-user="root" data-host="localhost">
  <code>
    cd /usr/local/etc
    cp php.ini php.ini.bak
    vi php.ini
  </code>
</pre>

<pre
  class="command-line language-bash"
  data-user="chris"
  data-host="remotehost"
  data-output="2, 4-8"
>
  <code>
    pwd
    /usr/home/chris/bin
    ls -la
    total 2
    drwxr-xr-x   2 chris  chris     11 Jan 10 16:48 .
    drwxr--r-x  45 chris  chris     92 Feb 14 11:10 ..
    -rwxr-xr-x   1 chris  chris    444 Aug 25  2013 backup
    -rwxr-xr-x   1 chris  chris    642 Jan 17 14:42 deploy
  </code>
</pre>
<!-- markdownlint-enable MD033 -->

#### Diff Highlight

Config:

```toml
[params.prism]
  languages = [
    "javascript",
    "diff"
  ]
  plugins = [
    "diff-highlight"
  ]
```

Input:

```html
<pre class="language-diff-javascript diff-highlight">
  <code>
    @@ -4,6 +4,5 @@
    -    let foo = bar.baz([1, 2, 3]);
    -    foo = foo + 1;
    +    const foo = bar.baz([1, 2, 3]) + 1;
         console.log(`foo: ${foo}`);
  </code>
</pre>
```

Output:

<!-- markdownlint-disable MD033 -->
<pre class="language-diff-javascript diff-highlight">
  <code>
    @@ -4,6 +4,5 @@
    - let foo = bar.baz([1, 2, 3]);
    - foo = foo + 1;
    + const foo = bar.baz([1, 2, 3]) + 1;
         console.log(`foo: ${foo}`);
  </code>
</pre>
<!-- markdownlint-enable MD033 -->
