# PSD Generator

A Python library for processing images and saving layers as PSD files.

## Prerequisites

Make sure you have [ImageMagick](https://imagemagick.org/index.php) installed. You can install it using the following commands:

### On Ubuntu/Debian:
```bash
sudo apt-get update
sudo apt-get install imagemagick
```

### On macOS:
You can install ImageMagick using [Homebrew](https://brew.sh/):
```bash
brew install imagemagick
```

### On Windows:
Download and install ImageMagick from the [official website](https://imagemagick.org/script/download.php).

## Installation

You can install the library using pip:

```bash
pip install my_image_processor
```

## Usage

Here is a basic example of how to use the library:

```python
from my_image_processor.processor import process_image

image_url = "https://example.com/image.jpg"
result = process_image(image_url, method_type=1, bandwidth=10, is_dynamic=1, num_colors=50)
print(result)
```

## Configuration

The `process_image` function takes the following parameters:

- `image_path` (str): URL or local path to the image file.
- `method_type` (int): Method type for processing (0 for default, 1 for custom).
- `bandwidth` (int): Bandwidth parameter for MeanShift clustering (used if `method_type` is 1).
- `is_dynamic` (int): Flag to use dynamic color extraction (1 for dynamic, 0 for predefined).
- `num_colors` (int): Number of dominant colors to extract (used if `is_dynamic` is 1).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.