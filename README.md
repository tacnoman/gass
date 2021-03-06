# Gass (Grep sASS)

[![Version](http://img.shields.io/npm/v/gass.svg)](https://www.npmjs.org/package/gass) [![Build Status](https://travis-ci.org/tacnoman/gass.svg?branch=master)](https://travis-ci.org/tacnoman/gass) [![Code Climate](https://codeclimate.com/github/tacnoman/gass/badges/gpa.svg)](https://codeclimate.com/github/tacnoman/gass) [![codecov](https://codecov.io/gh/tacnoman/gass/branch/master/graph/badge.svg)](https://codecov.io/gh/tacnoman/gass) [![HitCount](http://hits.dwyl.io/tacnoman/gass.svg)](http://hits.dwyl.io/tacnoman/gass)

Tool to get file and line using the css rule. When debugging css is difficult to get the css query and find in scss file.
With this tool you will find easy.

## Installation

```bash
$ npm i -g gass
```

## Usage

Create a scss file in a folder (ex: product.scss).

```scss
.product {
  &__title {
    color: #f00;

    &--active {
      color: #0f0;
    }
  }
}
```

Now run:

```bash
$ gass .product__title--active
```

You will see:

```bash
Searching in: **/*.scss

path/to/product.scss
5:    &--active {
```

## Change searcher

The default search is a glob `**/*.scss`, but is possible to search with another glob using the code:

```bash
$ gass .product__title--active -f stylesheets/**.scss
```
