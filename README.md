# PatternLab Base Toolkit

## Overview

This is merely just an attempt in a modular and reusable Design System using PatternLab.

This project is based on [PatternLab Node Edition Gulp](https://github.com/pattern-lab/edition-node-gulp).

Check out the [Technical Bits](#technical-bits) if you want to learn more about it.

## Design System

Based on different ideas and methodologies, I've tried to aim for something that is as comprehensive and clear as possible, which means that the following sections are currently covered (although most of the them are mostly a reference and need to be filled in appropriately):

1. **Rules**: (provided by [`starterkit-global-rules`](https://bitbucket.org/digitalrigbitbucketteam/starterkit-global-rules)) this can be summarised as the most important part of the Design System, it should cover areas like _personality_, _writing style_, _colours_, _illustrations_, _typography_, with simple and direct information on the principles behind each of them.
2. **Building Blocks**: (provided by [`starterkit-building-blocks`](https://bitbucket.org/digitalrigbitbucketteam/starterkit-building-blocks)`) this section includes more technical aspects, also considered the _foundation_ of the whole system, this includes areas like _illustrations_, _iconography_, _colours_ and their usage, _typography_. It can be also accompained with downloadable resources to be used in various media (emails, social media, ...).
3. **Patterns**: this section is what comes out of the above two points: it's essentially a pattern library that should feature elements that have been created.
4. **Applications**: this section covers practical examples of applications of the various components, possibly used as a way to document and test them.

The current implementation provides only a scheleton for this, moreover the various bits are going to be provided as separate dependencies that can be extended and improved or replaced as needed.

## Installation

Clone the current repo:

    $ git clone git@bitbucket.org:digitalrigbitbucketteam/patternlab-base-toolkit.git
    $ cd patternlab-base-toolkit

Install all the dependencies:

    $ npm install

Load the starterkits:

    $ gulp patternlab:loadstarterkit --kit=@buildit/starterkit-global-rules
    $ gulp patternlab:loadstarterkit --kit=@buildit/starterkit-building-blocks

Run the project:

    $ npm start

You can now access the website at <http://localhost:3000>.

## Technical bits

There are some major differences from the original project, namely:

- SASS compilation
- Directory structure
- Improved code standards to be used throughout the project

### SASS compilation

The `gulpfile.js` will automatically compile, inject, and reload the browser upon changes to any of the `*.scss` files available in the directory `/source/sass/`.

It comes with the following dependencies:

- [Eyeglass](http://eyeglass.rocks/) for enhanced npm module loading within the CSS.
- [Gravy](https://bitbucket.org/digitalrigbitbucketteam/gravy) very small SASS lib on steroids that handles typography and few other bits.

# TODO

- Add support for autoprefixer when compiling SCSS files.
- Add support for automatic SASS linting via stylelint.
