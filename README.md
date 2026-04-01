# pfm-to-colormap

PFM files to viridis colormap images in the browser.

## Features

- Load `.pfm` files by drag and drop or file selection
- Render with the **viridis** colormap
- Two display modes:
  - **log10 mode**: maps `log10(value)` to viridis
  - **linear mode**: maps raw float values to viridis
- Editable lower and upper bounds with instant re-render
- Mouse wheel zoom
- Drag to pan
- Show pixel float value while mouse button is pressed
- Export the rendered result as PNG

## Rules

### log10 mode
- Default range: `0.1` to `1000`
- `0` is treated as `0.0001`
- `float.MinValue` is shown in **blue**
- `float.MaxValue` is shown in **red**
- Other values are mapped with **viridis**

### linear mode
- Default range: `0` to `13`
- Values in the specified range are mapped with **viridis**

## Usage

1. Open the site
2. Drop a `.pfm` file, or select one from the file picker
3. Choose `log10` or `linear`
4. Adjust the min/max range if needed
5. Zoom with the mouse wheel and drag to move
6. Press the mouse button on the image to inspect the float value
7. Download the result as PNG

## Output filename

Exported PNG files are saved with the selected range in the filename.

Example:

```text
sample_min-0.1_max-1000.png
```

## GitHub Pages

This repository is intended to be published with GitHub Pages.

A typical URL will look like this:

```text
https://<username>.github.io/pfm-to-colormap/
```

## License

MIT License
See `LICENSE`.
