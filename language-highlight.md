# Language highlighting

Docsify uses [Prism](https://prismjs.com) to highlight code blocks in your pages. Prism supports the following languages by default:

* Markup - `markup`, `html`, `xml`, `svg`, `mathml`, `ssml`, `atom`, `rss`
* CSS - `css`
* C-like - `clike`
* JavaScript - `javascript`, `js`

Support for [additional languages](https://prismjs.com/#supported-languages) is available by loading the language-specific [grammar files](https://cdn.jsdelivr.net/npm/prismjs@1/components/) via CDN:

```html
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-bash.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-php.min.js"></script>
```

To enable syntax highlighting, wrap each code block in triple backticks with the [language](https://prismjs.com/#supported-languages) specified on the first line:

````
```html
<p>This is a paragraph</p>
<a href="//docsify.js.org/">Docsify</a>
```

```bash
echo "hello"
```

```php
function getAdder(int $x): int 
{
    return 123;
}
```
````

The above markdown will be rendered as:

```html
<p>This is a paragraph</p>
<a href="//docsify.js.org/">Docsify</a>
```

```bash
echo "hello"
```

```php
function getAdder(int $x): int 
{
    return 123;
}
```

```rpy
# Declare characters used by this game.
define s = Character(_("Sylvie"), color="#c8ffc8")
define m = Character(_("Me"), color="#c8c8ff")

# This is a variable that is True if you've compared a VN to a book, and False
# otherwise.
default book = False


# The game starts here.
label start:

    # Start by playing some music.
    play music "illurock.opus"

    scene bg lecturehall
    with fade

    "It's only when I hear the sounds of shuffling feet and supplies being put away that I realize that the lecture's over."

    "Professor Eileen's lectures are usually interesting, but today I just couldn't concentrate on it."

    "I've had a lot of other thoughts on my mind...thoughts that culminate in a question."

    "It's a question that I've been meaning to ask a certain someone."

```

## Highlighting Dynamic Content
Code blocks [dynamically created from javascript](https://docsify.js.org/#/configuration?id=executescript) can be highlighted using the method `Prism.highlightElement` like so:

```javascript
var code = document.createElement("code");
code.innerHTML = "console.log('Hello World!')";
code.setAttribute("class", "lang-javascript");
Prism.highlightElement(code);
```
