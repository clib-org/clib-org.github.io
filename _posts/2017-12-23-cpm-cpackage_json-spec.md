---
layout: post
title:  "cpackage.json Specification"
date:   2017-12-23 18:28:00 +0100
categories: cpm
---

### Detailed Specification

> To be continued 

### Full cpackage.json example

```json
{
  "name": "projectName",
  "version": "0.01",
  "description": "a json file to demonstrate how to use cpm",
  "license": "MIT",
  "url": "https://example.org",
  "bugtracker": "https://example.org",

  "authors": [
    {
      "name": "John Doe",
      "email": "john.doe@mail.com",
      "role": "owner"
    }
  ],

  "projects": {
    "example": {
      "path": "src/",
      "type": "binary",
      "lang": "c++",
      "linker": "-lncurses",
      "dependencies": {
        "libexample": "local",
        "otherdep": "pkg-config",
        "someLib": "1.0.2",
        "someOtherLib": "latest"
      }
    },

    "libexample": {
      "path": "lib/",
      "type": "library",
      "lang": "c++",
      "flags": "-Wall -Werror",
      "compiler": "std:c++11"
    },

    "example-test": {
      "path": "test/",
      "type": "test",
    },

    "external-test": {
      "type": "external-test",
      "command": "echo Test"
    }
  },

  "repositories": [
    {
      "type": "file",
      "url": "https://example.org/example.json",
      "priority": "low"
    }
  ],

  "commands": {
    "fetch": "git fetch",
    "push": "git push"
  }
}
```
