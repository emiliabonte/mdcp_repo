## Example 1: Simple Usage
<script>
function showCookies() {
  const output = document.getElementById('cookies')
  output.textContent = '> ' + document.cookie
}

function clearOutputCookies() {
  const output = document.getElementById('cookies')
  output.textContent = ''
}
</script>
<button onclick="showCookies()">Show cookies</button>

<button onclick="clearOutputCookies()">
  Clear
</button>

<div>
  <code id="cookies"></code>
</div>

## Example 2: Get a sample cookie named test2

<script>
// Note that we are setting `SameSite=None;` in this example because the example
// needs to work cross-origin.
// It is more common not to set the `SameSite` attribute, which results in the default,
// and more secure, value of `SameSite=Lax;`
document.cookie = "test1=Hello; SameSite=None; Secure";
document.cookie = "test2=World; SameSite=None; Secure";

const cookieValue = document.cookie
  .split('; ')
  .find(row => row.startsWith('test2='))
  .split('=')[1];

function showCookieValue() {
  const output = document.getElementById('cookie-value')
  output.textContent = '> ' + cookieValue
}

function clearOutputCookieValue() {
  const output = document.getElementById('cookie-value')
  output.textContent = ''
}
</script>
<button onclick="showCookieValue()">Show cookie value</button>

<button onclick="clearOutputCookieValue()">
  Clear
</button>

<div>
  <code id="cookie-value"></code>
</div>

## Example 3: Do something only once

<script>
function doOnce() {
  if (!document.cookie.split('; ').find(row => row.startsWith('doSomethingOnlyOnce'))) {
    // Note that we are setting `SameSite=None;` in this example because the example
    // needs to work cross-origin.
    // It is more common not to set the `SameSite` attribute, which results in the default,
    // and more secure, value of `SameSite=Lax;`
    document.cookie = "doSomethingOnlyOnce=true; expires=Fri, 31 Dec 9999 23:59:59 GMT; SameSite=None; Secure";

    const output = document.getElementById('do-once')
    output.textContent = '> Do something here!'
  }
}

function clearOutputDoOnce() {
  const output = document.getElementById('do-once')
  output.textContent = ''
}
</script>
<button onclick="doOnce()">Only do something once</button>

<button onclick="clearOutputDoOnce()">
  Clear
</button>

<div>
  <code id="do-once"></code>
</div>

## Example 4: Reset the previous cookie

<script>
  function resetOnce() {
  // Note that we are setting `SameSite=None;` in this example because the example
  // needs to work cross-origin.
  // It is more common not to set the `SameSite` attribute, which results in the default,
  // and more secure, value of `SameSite=Lax;`
  document.cookie = "doSomethingOnlyOnce=; expires=Thu, 01 Jan 1970 00:00:00 GMT; SameSite=None; Secure";

  const output = document.getElementById('reset-once')
  output.textContent = '> Reset!'
}

function clearOutputResetOnce() {
  const output = document.getElementById('reset-once')
  output.textContent = ''
}
</script>
<button onclick="resetOnce()">Reset only once cookie</button>

<button onclick="clearOutputResetOnce()">
  Clear
</button>

<div>
  <code id="reset-once"></code>
</div>

## Example 5: Check a cookie existence

<script>
  // Note that we are setting `SameSite=None;` in this example because the example
// needs to work cross-origin.
// It is more common not to set the `SameSite` attribute, which results in the default,
// and more secure, value of `SameSite=Lax;`
document.cookie = "reader=1; SameSite=None; Secure";

function checkACookieExists() {
  if (document.cookie.split(';').some((item) => item.trim().startsWith('reader='))) {
    const output = document.getElementById('a-cookie-existence')
    output.textContent = '> The cookie "reader" exists'
  }
}

function clearOutputACookieExists() {
  const output = document.getElementById('a-cookie-existence')
  output.textContent = ''
}
</script>
<button onclick="checkACookieExists()">
  Check a cookie exists
</button>

<button onclick="clearOutputACookieExists()">
  Clear
</button>

<div>
  <code id="a-cookie-existence"></code>
</div>

## Example 6: Check that a cookie has a specific value

<script>
  function checkCookieHasASpecificValue() {
  if (document.cookie.split(';').some((item) => item.includes('reader=1'))) {
    const output = document.getElementById('a-specific-value-of-the-cookie')
    output.textContent = '> The cookie "reader" has a value of "1"'
  }
}

function clearASpecificValueOfTheCookie() {
  const output = document.getElementById('a-specific-value-of-the-cookie')
  output.textContent = ''
}
</script>
<button onclick="checkCookieHasASpecificValue()">
  Check that a cookie has a specific value
</button>

<button onclick="clearASpecificValueOfTheCookie()">
  Clear
</button>

<div>
  <code id="a-specific-value-of-the-cookie"></code>
</div>


## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/emiliabonte/mdcp_repo/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/emiliabonte/mdcp_repo/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

