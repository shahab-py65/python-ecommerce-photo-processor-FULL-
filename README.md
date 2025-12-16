# E-commerce Product Photo Processor (Professional CLI Tool)

A fully customizable Python command-line tool for bulk product image processing – ideal for Shopify, Amazon, Etsy, and online stores.

## Features
- AI-powered automatic background removal (rembg)
- Resize to custom size with clean white background
- Add logo watermark (position, size, opacity, margin fully adjustable)
- Batch processing hundreds/thousands of images
- Easy to use via command line arguments

## Demo

### Before
![Before](photos/before.jpg)

### After
![After](processed/after.jpg)

## Installation
```bash
pip install pillow rembg

Bash
python FcuL.py \
  --input photos \
  --output processed \
  --logo logo.png \
  --size 1000 \
  --logo-percent 15 \
  --position bottom-right \
  --opacity 180 \
  --margin 50

Bash
python FcuL.py --help

Technologies

Python
Pillow
rembg (AI background removal)
argparse

usage: FcuL.py [-h] --input INPUT --output OUTPUT --logo LOGO [--size SIZE] ...

options:
  -h, --help            show this help message and exit
  --input INPUT         Input folder path
  --output OUTPUT       Output folder path
  --logo LOGO           Logo image path (PNG recommended)
  --size SIZE           Max width/height for resize (default: 1000)
  --logo-percent LOGO_PERCENT
                        Logo size as percent of image width (default: 15)
  --position {bottom-right,bottom-left,top-right,top-left}
                        Logo position (default: bottom-right)
  --opacity OPACITY     Logo opacity (0-255, default: 180)
  --margin MARGIN       Margin from edges in pixels (default: 50)
