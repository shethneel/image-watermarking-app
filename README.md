# MarkIt : Image watermarking tool

This Python project provides functionality to add **image watermarks** or **text watermarks** to an image. 
It utilizes popular libraries like `requests`, `cv2`, `Pillow`, and `NumPy` to process and manipulate images. 
This tool allows for customizable watermarks, enabling users to enhance their images with logos or text.

---

## Features

- **Image Watermarking**: Adds a logo image as a watermark to the bottom-right corner of the main image.
- **Text Watermarking**: Adds customizable text as a watermark to the image.
- **Customizations**:
  - Resizable logo for image watermarking.
  - Selectable font styles and colors for text watermarking.
  - Adjustable positions and margins.

---

## Requirements

To run this project, you need the following Python packages installed:

- `requests`
- `opencv-python` (`cv2`)
- `numpy`
- `Pillow`

Install these dependencies using pip:

`pip install requests opencv-python numpy pillow`

## How It Works

### 1. Image Watermarking
- Prompts the user to upload a logo image.
- Places the logo at the bottom-right corner of the base image with customizable size and margins.

### 2. Text Watermarking
- Prompts the user to input text.
- Allows selection of font style and text color in BGR format.
- Adds the text to the image at a default or user-specified position.

## How to Run

1. Clone the repository and navigate to the project folder.
2. Run the script:

`python MarkIt.py`

3. Follow the on-screen instructions to choose between image or text watermarking.

## Input Details

- **Base Image**: The base image is loaded from a URL and resized to `(500x300)` for simplicity.
- **Logo Image** (for image watermarking): Provide the file path to your logo image (e.g., `/path/to/logo.jpg`).
- **Text** (for text watermarking): Input the desired text, font style, and BGR color values.

## Code Overview

### Main Functions

#### `add_logo_watermark`
- **Description**: Adds a logo image to the bottom-right corner of the base image.
- **Parameters**:
  - `img`: Base image (`PIL.Image`).
  - `logo_path`: Path to the logo image.
  - `logo_size`: Tuple specifying the dimensions of the logo.
  - `margin`: Space between the logo and the image edges.

#### `add_text_watermark`
- **Description**: Adds customizable text to the base image.
- **Parameters**:
  - `img`: Base image (`PIL.Image`).
  - `text`: Text to be added as a watermark.
  - `position`: Tuple specifying the coordinates of the text.
  - `font`: Font style for the text.
  - `font_scale`: Font size for the text.
  - `color`: Color of the text in BGR format.
  - `thickness`: Thickness of the text.

#### `main`
- **Description**: Handles user interaction and calls the appropriate watermarking function based on the user's choice.

## Example Usage

### Image Watermarking
1. Select option `1` when prompted.
2. Provide the path to your logo image (e.g., `/content/google.jpg`).
3. The watermarked image will be displayed with the logo in the bottom-right corner.

### Text Watermarking
1. Select option `2` when prompted.
2. Input the desired text, font style, and color in BGR format.
3. The watermarked image with text will be displayed.

---

## Output

- The watermarked images are displayed directly in the notebook environment using `cv2_imshow`.
- You can modify the script to save the output images locally.

---

## Error Handling

- Handles invalid user inputs (e.g., non-integer choices or invalid file paths).
- Provides descriptive error messages for debugging.

---

## Author

This project was developed as an image processing tool to demonstrate watermarking techniques using Python.

Feel free to modify and enhance the functionality as per your requirements!
