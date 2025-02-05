# About

This is a demo of the the `srcset` and `sizes` attributes of the html `img` tag.

[Skip to the demo](#demo)

## What is the srcset attribute?
The srcset attribute is a method of displaying responsive images.  It provides the browser with additional information allowing it to choose the most appropriate image for the current device.

For a given `img` element, the `srcset` attribute can be used to supply a range of responsive images to the browser along with size information to help the browser choose the correct image.

> Shortly after the browser downloads the HTML, it requests CSS and JavaScript. But before the CSS and JavaScript is done loading, the browser starts downloading images.

> Because neither the CSS nor JavaScript is complete, the browser is downloading images without knowing what the layout of the page will be. And without knowing the layout, it doesn’t know what size the image element will be.

- http://blog.cloudfour.com/responsive-images-101-part-4-srcset-width-descriptors/

The srcset attribute provides the browser with the image size information it needs:

```
<img src="image1.jpg" alt=""
    srcset="
      image1.jpg 300w,
      image1-b.jpg 600w,
      image1-c.jpg 1200w"
>
```

## What is sizes?
> Like srcset, the sizes attribute contains a comma-separated list. This comma-separated list describes the size of the image in relation to the viewport.

- http://blog.cloudfour.com/responsive-images-101-part-5-sizes/

```
<img src="image1.jpg" alt=""
    srcset="
      image1.jpg 300w,
      image1-b.jpg 600w,
      image1-c.jpg 1200w
    "
    sizes="
      100vw
      (min-width:600px) 66vw,
      (min-width:960px) 50vw,
    "
>
```

If the sizes attribute is left out, the browser will assume that all images are displayed at 100% of the viewport width.

## What about the picture element?
The picture element can be used for art direction when handling responsive images.

## Demo
Use this demo to see how the browser decides to load different images on the page.  Start with a narrow window and increase the width.  Try with a retina device.  

Note that the browser will not display a lower-res image once it's cached a higher-res alternative, remember to clear your cache between page loads.

- [View demo](index.html)

# Resources
Browser support:
- https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/

W3C Spec:
- https://html.spec.whatwg.org/multipage/embedded-content.html#attr-img-srcset

Articles:
- http://blog.cloudfour.com/dont-use-picture-most-of-the-time/
- https://ericportis.com/posts/2014/srcset-sizes/
- https://ericportis.com/posts/2014/separated/
- https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/
- http://blog.cloudfour.com/responsive-images-101-definitions/

# License

Images generated via http://lorempixel.com.  Each image is licensed under the creative commons license [CC BY-SA](https://creativecommons.org/licenses/by-sa/3.0/).

The remaining files in this repo are [MIT licensed](http://opensource.org/licenses/MIT)
