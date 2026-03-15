# Create a GIF with Python 🎞️

A simple Python script that combines multiple images into an animated GIF in just 6 lines of code! This project is based on the [Codédex tutorial](https://www.codedex.io/projects/create-a-gif-with-python) by Sonny Li. 

## Description
Graphics Interchange Format (GIF) is a popular image format used to display simple animations, operating much like a digital flipbook. This project demonstrates how to use Python's `imageio` library to read a sequence of static images and stitch them together into a looping GIF.

## Prerequisites
Before running this project, ensure you have the following installed:
* **Python** (Version 3.10 or higher recommended)
* **pip** (Python package installer)
* Command Line / Terminal fundamentals

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/create-a-gif-with-python.git
   cd create-a-gif-with-python
   ```

2. **Install the required library:**
   This project relies on `imageio` (version 2.16.2 or higher). Install it via pip:
   ```bash
   pip3 install imageio
   ```
   *(Note: You can verify the installation by opening your Python IDLE and typing `import imageio`. If no errors appear, you are good to go!)*

## Usage

1. **Prepare your images:**
   Place the images you want to animate inside the same directory as your Python script. Ensure they all share the exact same width and height for the best results.

2. **Update the code:**
   Open `create_gif.py` and update the `filenames` list with your actual image file names:
   ```python
   import imageio.v3 as iio

   # Replace with your image file names
   filenames = ['team-pic1.png', 'team-pic2.png']
   images = []

   for filename in filenames:
       images.append(iio.imread(filename))

   # Generate the GIF
   iio.imwrite('team.gif', images, duration=500, loop=0)
   ```

3. **Run the program:**
   Execute the script from your terminal:
   ```bash
   python3 create_gif.py
   ```

4. **View your GIF:**
   A new file named `team.gif` will be generated in the same folder. Open it to see your custom animation!

## How it Works
* `iio.imread(filename)`: Reads the visual data of each image path provided in the list.
* `iio.imwrite('team.gif', ...)`: Compiles the loaded images into a single file.
* `duration=500`: Sets the display time for each frame to 500 milliseconds (half a second).
* `loop=0`: Tells the GIF to loop infinitely.

## Credits
* Tutorial and project inspiration from [Codédex](https://www.codedex.io/).
