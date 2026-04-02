# pfm-to-colormap

Visualize `.pfm` and `.csv` numeric data in the browser with **viridis** or **jet**, then export the result as PNG.

## Features

- Load `.pfm` and `.csv` files by drag and drop or file selection
- Two colormaps:
  - **viridis**
  - **jet**
- Two display modes:
  - **log10 mode**
  - **linear mode**
- Editable lower and upper bounds with instant re-render
- Mouse wheel zoom
- Drag to pan
- Show pixel float value while the mouse button is pressed
- Export the rendered result as PNG

## Display rules

### log10 mode
- Default range: `0.1` to `1000`
- `0` is treated as `0.0001`
- `float.MinValue` is shown in **blue**
- `float.MaxValue` is shown in **red**
- Other values are mapped with the selected colormap

### linear mode
- Default range: `1` to `13`
- Values in the specified range are mapped with the selected colormap

### Colormap direction
- **viridis**: low → high
- **jet**: low = blue, high = red

## CSV input

This app can also read numeric `.csv` files.

Expected format:
- The first row may be a metadata row such as `321,428,0`
- The following rows are treated as the numeric matrix to display

## Usage

1. Open the site
2. Drop a `.pfm` or `.csv` file, or select one from the file picker
3. Choose `log10` or `linear`
4. Choose `viridis` or `jet`
5. Adjust the min/max range if needed
6. Zoom with the mouse wheel and drag to move
7. Press the mouse button on the image to inspect the value
8. Download the result as PNG

## Output filename

Exported PNG files include the selected colormap and range in the filename.

Example:

```text
sample_jet_min-0.1_max-1000.png
```

## GitHub Pages

This repository is intended to be published with GitHub Pages.

Typical URL:

```text
https://<username>.github.io/pfm-to-colormap/
```

## License

MIT License  
See `LICENSE`.
