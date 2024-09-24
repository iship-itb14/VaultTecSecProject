# VaultTecSecProject
Image Encoder Steganography
This project is a simple Image Steganography tool that encodes and decodes hidden messages within image files using Least Significant Bit (LSB) steganography. The project includes an encoding tool to hide text inside images and a decoding tool to reveal the hidden messages.

Features
Encode: Hide secret messages within images.
Decode: Retrieve hidden messages from encoded images.
Tkinter Interface: A user-friendly graphical interface built using Tkinter.
Python Script: Core functionality implemented in Python.
Requirements
Python 3.x
Required Libraries:
Pillow (for image manipulation)
Stegano (for LSB steganography)
Tkinter (for GUI)
Install Requirements
Run the following command to install required Python libraries:

bash
Copy code
pip install pillow stegano
How It Works
1. Encoding (Hiding the Message)
The encoding process embeds a secret message inside an image file using the Least Significant Bit (LSB) steganography technique. The altered pixels are imperceptible to the human eye, ensuring the image looks unchanged.

2. Decoding (Revealing the Message)
The decoding process retrieves the secret message from the altered pixels of the encoded image.

Usage
Encode a Message into an Image
To encode a message into an image, use the following Python code:

python
Copy code
from stegano import lsb

# Load the image and encode the message
lsb.hide("original_image.png", "encoded_image.png", "Secret Message")
original_image.png: The image file you want to hide the message in.
encoded_image.png: The output image file with the encoded message.
Secret Message: The message to be hidden.
Decode a Hidden Message from an Image
To decode and retrieve a hidden message from an encoded image, use the following Python code:

python
Copy code
from stegano import lsb

# Reveal the hidden message from the image
secret_message = lsb.reveal("encoded_image.png")
print("Hidden Message:", secret_message)
encoded_image.png: The image file containing the hidden message.
