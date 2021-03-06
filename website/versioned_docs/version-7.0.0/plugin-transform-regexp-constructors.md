---
id: version-7.0.0-babel-plugin-transform-regexp-constructors
title: babel-plugin-transform-regexp-constructors
sidebar_label: transform-regexp-constructors
original_id: babel-plugin-transform-regexp-constructors
---

## Example

**In**

```javascript
const foo = 'ab+';
var a = new RegExp(foo+'c', 'i');
```

**Out**

```javascript
const foo = 'ab+';
var a = /ab+c/i;
```

## Installation

```sh
npm install babel-plugin-transform-regexp-constructors --save-dev
```

## Usage

### With a configuration file (Recommended)

```json
{
  "plugins": ["transform-regexp-constructors"]
}
```

### Via CLI

```sh
babel --plugins transform-regexp-constructors script.js
```

### Via Node API

```javascript
require("@babel/core").transform("code", {
  plugins: ["transform-regexp-constructors"]
});
```

