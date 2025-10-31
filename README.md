# Pencil_Sketch_Effect
Transform your digital photographs into beautiful pencil sketch artwork using advanced image processing techniques. This application provides multiple sketch styles and real-time processing capabilities.
# 🎨 Overview
The Pencil Sketch Effect is a computer vision application that converts regular photographs into pencil sketch-style artwork using OpenCV image processing techniques. Whether you want to create artistic portraits, add creative filters to your photos, or experiment with real-time video effects, this tool makes it simple and accessible.
# ✨ Key Features

- Grayscale Pencil Sketch: Classic black and white sketch conversion using manual image processing pipeline
- Colored Pencil Sketch: Advanced colored sketch effect with customizable parameters
- Real-Time Webcam Filter: Live video processing with instant sketch preview
- Save & Export: Easy image saving with automatic format handling
- Side-by-Side Comparison: View original and sketch versions simultaneously
- Interactive Controls: User-friendly menu system with simple navigation

# 🖼️ Demo
- Grayscale Sketch
Original image transformed into realistic pencil sketch with edge highlighting and natural shading.
- Colored Sketch
Artistic colored pencil effect preserving color information while adding sketch-like textures.
- Real-Time Processing
Live webcam feed with instant sketch filter application.
# 🚀 Getting Started
Prerequisites:

- Python 3.6 or higher
- Webcam (optional, for real-time features)
- 4GB RAM minimum

Run the application:
bashpython pencil_sketch.py
```

Follow the interactive menu:
```
1. Image to Pencil Sketch - Convert static images to grayscale sketches
2. Image to Colored Sketch - Create colored pencil artwork
3. Webcam Pencil Sketch - Real-time video sketch filter
4. Exit
```

## 🔧 Technical Details

### Core Image Processing Techniques

#### Grayscale Sketch Algorithm
```
1. Load Image → Read input using OpenCV
2. Convert to Grayscale → Remove color information
3. Invert Grayscale → Create negative image
4. Apply Gaussian Blur → Blur inverted image (21×21 kernel)
5. Invert Blurred Image → Second inversion
6. Divide Images → Gray ÷ Inverted blurred
7. Scale Result → Multiply by 256
8. Output → Realistic pencil sketch
```

**Core Formula:**

 Sketch = (Gray Image / Inverted Blurred Image) × 256
``` 
This technique:

- Highlights edges and fine details
- Simulates natural pencil strokes
- Creates light/shadow contrast
- Mimics hand-drawn appearance

Colored Sketch Algorithm
- Uses OpenCV's built-in pencilSketch() function:
- pythoncv2.pencilSketch(image, sigma_s=60, sigma_r=0.07, shade_factor=0.05)
```

**Parameters:**
- `sigma_s (60)`: Spatial window size - controls smoothness
- `sigma_r (0.07)`: Range window size - controls color preservation
- `shade_factor (0.05)`: Controls shading intensity

### Code Architecture

**Modular Design with Three Main Functions:**

1. **`pencil_sketch()`**
   - Basic grayscale sketch conversion
   - Manual image processing pipeline
   - Single output image

2. **`pencil_sketch_colored()`**
   - Advanced colored sketch effect
   - Dual output (grayscale and colored)
   - Adjustable parameters

3. **`webcam_pencil_sketch()`**
   - Real-time video processing
   - Frame-by-frame conversion
   - Interactive controls (Press 'S' to save, 'Q' to quit)

## 📋 Features Breakdown

### Static Image Processing
✓ Load images from any path  
✓ Multiple format support (JPG, PNG, BMP, TIFF)  
✓ Side-by-side comparison view  
✓ Optional save functionality  
✓ Automatic file extension handling  
✓ High-quality output preservation  

### Real-Time Webcam Processing
✓ Live video processing at smooth frame rates  
✓ Side-by-side original and sketch view  
✓ Interactive screenshot capture (Press 'S')  
✓ Easy exit option (Press 'Q')  
✓ No lag or frame drops  

### User Interface
✓ Clear menu navigation  
✓ Input validation and error handling  
✓ Path handling with quote removal  
✓ Save prompts and confirmations  
✓ Status messages and feedback  

## 💡 Applications

### Real-World Use Cases
- **Digital Art**: Create artistic renditions of photographs
- **Photography**: Add creative effects to portrait photos
- **Education**: Teach image processing and computer vision concepts
- **Content Creation**: Social media filters and effects
- **Profile Pictures**: Generate unique artistic avatars
- **Design**: Quick sketch mockups for creative projects
- **Printing**: Prepare images for print sketches

## 📊 Input/Output Specifications

### Input Requirements
- Any standard image format (JPG, PNG, BMP, TIFF)
- Clear, well-lit photographs work best
- Portrait or landscape orientation supported
- Minimum recommended resolution: 640×480

### Output Quality
- Same resolution as input image
- Grayscale or colored options
- JPEG format (default)
- Maintains original aspect ratio
- High-quality preservation

## ⚙️ Technical Implementation

### Why Gaussian Blur Works
- Smooths harsh transitions
- Reduces image noise
- Creates softer, more natural sketch lines
- Prevents over-sharpening artifacts

### Image Division Technique
The division operation creates the sketch effect by:
- Enhancing edge information
- Creating natural contrast
- Simulating pencil pressure variations
- Producing realistic shading

## 🎯 Advantages

✓ **Easy to Use**: Simple menu-driven interface, no technical knowledge required  
✓ **Fast Processing**: Efficient OpenCV algorithms for quick results  
✓ **Versatile**: Multiple sketch styles and processing modes  
✓ **Real-Time Capable**: Live webcam processing without lag  
✓ **Free & Open Source**: Built with open-source libraries  
✓ **Customizable**: Adjustable parameters for fine-tuning  
✓ **Offline**: No internet connection required  

## 🔮 Future Enhancements

### Planned Improvements
- **GUI Development**: Add graphical interface using Tkinter or PyQt
- **Batch Processing**: Process multiple images simultaneously
- **Parameter Sliders**: Real-time adjustable settings
- **Additional Filters**: Oil painting, watercolor, charcoal effects
- **Video File Support**: Process recorded video files
- **Mobile App**: Android/iOS application development
- **AI Enhancement**: Deep learning-based sketch generation
- **Style Transfer**: Multiple artistic style options
- **Edge Detection Options**: Canny, Sobel, and custom algorithms
- **Export Formats**: PNG, SVG, PDF output options

## 🚧 Current Limitations

- Limited to predefined parameters (hardcoded values)
- Command-line interface only (no GUI)
- Single image processing at a time
- Fixed Gaussian blur kernel size (21×21)
- No undo/redo functionality
- Limited artistic style variations

## 📦 Project Structure

pencil-sketch-effect/
├── pencil_sketch.py          # Main application
├── README.md                 # Documentation
├── requirements.txt          # Dependencies
├── examples/                 # Sample images
│   ├── input/
│   └── output/
└── screenshots/              # Demo screenshots
    ├── grayscale_demo.jpg
    ├── colored_demo.jpg
    └── webcam_demo.jpg
```
# 🛠️ Dependencies
- txtopencv-python>=4.5.0
- numpy>=1.19.0
# 📚 Learning Resources

- OpenCV Documentation
- NumPy Library
- Python Official Site
- Digital Image Processing Fundamentals
- Computer Vision Research Papers
# 📄 License
This project is open source and available under the MIT License.
