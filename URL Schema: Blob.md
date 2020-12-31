---
title: Hello World
tags: ['tag1', 'tag2']
---


Blob URL/Object URL is a pseudo protocol to allow Blob and File objects to be used as URL source for things like images, download links for binary data and so forth.

Example: `blob:https://crap.io/media/me.jpg`

### Validity of a Object URL(Blob)

Blob URLs can only be generated internally by the browser.

1.  Can be used only by a Single Browser Instance
2.  Can be used only in Same Session(i.e. life of the page/document)

### Creation and Revocation

1.  [`URL.createObjectURL()`](https://developer.mozilla.org/en-US/docs/Web/API/URL/createObjectURL)
2.  [`URL.revokeObjectURL()`](https://developer.mozilla.org/en-US/docs/Web/API/URL/revokeObjectURL)

### Reference

1.  https://stackoverflow.com/a/30881444/8657006
