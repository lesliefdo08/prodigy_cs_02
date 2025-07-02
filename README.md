# Leslie Fernando prodigy_cs_02
Image Encryption &amp; Decryption

This Python script allows users to **encrypt (lock)** and **decrypt (unlock)** images using a basic pixel-based transformation method. It shifts pixel values using a fixed secret key to obscure the original image and later restores it using the reverse operation.

Features:

* Locks (encrypts) an image using pixel value manipulation
* Unlocks (decrypts) the image back to its original form
* Simple to use from the terminal
* Keeps file format and size unchanged

How it works:

* Each pixel value (RGB) in the image is increased by a fixed `SECRET_KEY` value (modulo 256) during encryption.
* Decryption subtracts the same `SECRET_KEY` to retrieve the original image.
* Uses Python Imaging Library (PIL) and NumPy for image processing.

Sample Terminal Output:

1. Locking Example
   Enter original image path: `sample.jpg`
   Save encrypted image as: `encrypted.jpg`
   Image successfully locked and stored at: encrypted.jpg

2. Unlocking Example
   Enter encrypted image path: `encrypted.jpg`
   Save decrypted image as: `unlocked.jpg`
   Image successfully unlocked and saved at: unlocked.jpg

How to Run:

1. Save the script as `image_locker.py`
2. Make sure `Pillow` and `NumPy` are installed:
   pip install pillow numpy

3. Run the script:
   python image_locker.py
   
4. Follow the on-screen prompts to lock or unlock an image.

Note:
The `SECRET_KEY` is fixed at 50. Changing this value without re-encrypting will not give accurate results during decryption.

