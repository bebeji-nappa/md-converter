# Md Converter
This tool make Markdown syntax convert to HTML syntax.

## [WARNING] Md Converter is finishing support at 2021/06.
I'm Sorry, As we prepare for the release of **[RichMD.js](https://github.com/bebeji-nappa/richmdjs)** Major version, Md Converter is finishing support at 2021/06. 

RichMD.js has not only basic Markdown support but also various functions is had by Original Syntax.

We apologize for the inconvenience, but please migrate to RichMD.js .

*This is wrote at 2020/12/22.*

## Installation

```bash
# use npm
npm install md-converter

# use yarn
yarn add md-converter
```

## Usage
### ES Module
You can use Md Converter as a ECMAScript module.

```js
import { mdConvert } from 'md-converter'

const md = `# heading 1`
mdConvert(md) // Markdown convert to HTML
```

### Vue.js
#### Simple example usage

```js
<template>
  <form id="post-form">
    <div id="editor">
      <textarea v-model="markdownText" class="textField"></textarea>
    </div>
    <div id="preview">
      <div v-html="compiledMarkdown" class="preview"></div>
    </div>
  </form>
</template>
<script>
import { mdConvert } from 'md-converter'

export default {
  data() {
    return {
      markdownText: ''
    }
  },
  computed: {
    compiledMarkdown () {
      return mdConvert(this.markdownText)
    }
  },
}
</script>
```

## Suport Syntax
- strong
- italic
- image
- link
- headings
- horizontal rule
- blockquote
- unordeed list
- ordeed list
- strikethrough
- code block
- checkbox list
- table
