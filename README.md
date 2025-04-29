# Steganographyx





 Project Structure- The Steganographyx project is organized into two main sections: Image Steganography and Wave Audio Steganography. Each section has its set of classes and methods:
Image Steganography:

Encode class: Handles encoding (hiding) secret messages within images.
Decode class: Handles decoding (extracting) secret messages from images.

# What is steganography?

Steganography is the technique of hiding data within an ordinary, nonsecret file or message to avoid detection; the hidden data is then extracted at its destination. Steganography use can be combined with encryption as an extra step for hiding or protecting data. The word steganography is derived from the Greek word steganos, meaning "hidden or covered," and the Greek root graph, meaning "to write."

Steganography can be used to conceal almost any type of digital content, including text, image, video or audio content. The secret data can be hidden inside almost any other type of digital content. The content to be concealed through steganography -- called hidden text -- is often encrypted before being incorporated into the innocuous-seeming cover text file or data stream. If not encrypted, the hidden text is commonly processed in some method to increase the difficulty of detecting the secret content.

# Overview
The steganography program provided is a Python application that facilitates hiding and extracting secret messages in various media, including images and wave audio files. The program utilizes cryptographic techniques to encode and decode messages securely.

## Installation

To use Steganographyx, follow these steps:

1. Clone the repository:
```
git clone https://github.com/athrvadeshmukh/Steganographyx.git
```

# Libraries
Ensure you have the following Python libraries installed to run the program:

# PIL (Pillow): Used for image processing and displaying a logo in the GUI.
```
pip install Pillow
```

# Crypto.Cipher (PyCryptoDome): Provides cryptographic algorithms for secure message encoding and decoding.
```
pip install pycryptodome
```

# NumPy: Purpose: Required for numerical operations, especially in the image steganography program.
```
pip install numpy
```

# 1. Image Steganography
class Encode
Purpose: Handles encoding (hiding) secret messages within images.
Methods:
__init__(image_path, password, text_to_encode): Initializes the Encode object with the image path, password, and text to be encoded.
is_password_valid(): Checks if the supplied password is valid.
is_text_valid(): Checks if the supplied text to be encoded is valid.
is_image_path_valid(): Checks if the supplied image path is valid and the image file exists.
get_text_binary(): Generates the binary equivalent of the text to be encoded.
encode_into_image(): Hides/encodes the binary data into the image using LSB modification.
are_values_valid(): Validates the password, image path, and text before encoding.
class Decode
Purpose: Handles decoding (extracting) secret messages from images.
Methods:
__init__(image_path, password): Initializes the Decode object with the image path and password.
is_password_valid(): Checks if the supplied password is valid.
is_image_path_valid(): Checks if the supplied image path is valid and the image file exists.
get_decoded_text(bytes_string): Decrypts the extracted bytes string to obtain the original text.
decode_from_image(): Extracts the encoded binary data from the image.
are_values_valid(): Validates the password and image path before decoding.

# How to Run
Ensure the required libraries are installed (Pillow, pycryptodome, Numpy, Tkinter, Wave).
Run the respective scripts for image steganography (encryptstego.py) or wave audio steganography (encode_audio.py and decode_audio.py).
Follow the GUI instructions to select input files, enter messages, and perform encoding or decoding.

# Notes
Image steganography modifies the least significant bit (LSB) of each pixel's channels to hide the message.




![Screenshot 2023-11-08 215347](https://github.com/athrvadeshmukh/Steganography/assets/112002659/95687878-500f-470a-88a4-af81c3d83dcd)

![Screenshot 2023-11-08 215403](https://github.com/athrvadeshmukh/Steganography/assets/112002659/32b23071-ed10-42bc-82d5-b0e53fb4d05f)
