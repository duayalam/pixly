# Pixly.js 🖼️

A lightweight, feature-rich, and secure image viewer for the web.

## Quick Start (CDN)

Simply include the following script in your HTML. Pixly automatically injects its own styles, so you only need one file:

```html
<script src="https://cdn.jsdelivr.net/gh/duayalam/pixly@1.0.0/dist/pixly.min.js"></script>
```

---

## How to Use

### 1. Auto-detected HTML Gallery

Wrap your images in a container and initialize Pixly using a selector. It will automatically detect images and set up the click events.

**HTML:**

```html
<div class="my-gallery">
  <img
    src="image1.jpg"
    data-title="Cool Image"
    data-description="This is an awesome description."
  />
  <img src="image2.jpg" alt="Minimal fallback title" />
</div>
```

**JavaScript:**

```javascript
new Pixly(".my-gallery", {
  loop: true,
  showTitle: true,
  showDescription: true,
});
```

### 2. Manual Array Gallery

You can also open a gallery from a button click using a custom data array.

**JavaScript:**

```javascript
const myImages = [
  { src: "img1.jpg", title: "Image 1", description: "Desc 1" },
  { src: "img2.jpg", title: "Image 2", description: "Desc 2" },
];

const viewer = new Pixly(myImages);

// Open manually at index 0
document.getElementById("openBtn").onclick = () => viewer.open(0);
```

---

## Configuration Options

| Option            | Type    | Default | Description                                              |
| :---------------- | :------ | :------ | :------------------------------------------------------- |
| `loop`            | boolean | `true`  | Allows continuous navigation (last image back to first). |
| `showTitle`       | boolean | `true`  | Displays the image title in the viewer header.           |
| `showDescription` | boolean | `true`  | Displays the image description below the title.          |
| `showTools`       | boolean | `true`  | Shows the floating toolbar (Zoom, Rotate, Flip, etc.).   |

---

## Features

- ✅ **Smooth Zoom**: Use buttons or mouse wheel anywhere.
- ✅ **Ultra-Fluid Drag**: GPU-accelerated dragging to explore zoomed images.
- ✅ **Transformations**: Support for 90° rotation and H/V flipping.
- ✅ **Smart UI**: Modern floating toolbar with backdrop-filter.
- ✅ **Secure**: Built-in "Self-Defending" obfuscation against code tampering/beautifying.

---

**Note:** This distributed version is obfuscated for protection. Attempting to format or modify the file will cause it to stop working.
