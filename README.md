# Image Encryption Tool

This Python script encrypts and decrypts images using a simple pixel swapping technique. It utilizes the Pillow (PIL) library for image manipulation.

## Features

* **Image Encryption:** Encrypts an image by swapping red and green pixel values based on a user-provided key.
* **Image Decryption:** Decrypts an encrypted image using the same key used for encryption.
* **Handles RGB Images:** The script is designed to work with RGB images. It includes error handling for RGBA images, and converts them to RGB before processing.

## Prerequisites

* Python 3.x
* Pillow (PIL) library: Install using `pip install Pillow`

## Usage

1. **Clone the Repository:**

 bash
 git clone [https://github.com/Kalyan16114421/Image-Encryption-Tool]
 cd [Image-Encryption-Tool]

2. **Prepare an Image:**

 * Place an image file (e.g., `image.jpg` or `image.png`) in the same directory as the Python script or provide the full path to the image in the `original_image` variable.

3. **Run the Script:**

 ```bash
 python image_encryption.py
 ```

4. **Modify the Code (Optional):**

 * Change the `original_image` variable to the path of your image.
 * Modify the `secret_key` variable to use a different encryption/decryption key.
 * Change the output paths for the encrypted and decrypted images if needed.

## Code Explanation

* **`encrypt_image(image_path, key)`:**
 * Opens the image file.
 * If image is in PNG or other form Converts images to JPG.
 * Iterates through the pixels and swaps red and green values based on the key.
 * Saves the encrypted image.

* **`decrypt_image(encrypted_image, key)`:**
 * Opens the encrypted image.
 * Iterates through the pixels and swaps red and green values back to their original positions based on the key.
 * Saves the decrypted image.

## Example
```python
original_image = r"C:\path\to\your\image.png" # Replace with your image path
secret_key = 3

encrypted_img = encrypt_image(original_image, secret_key)
if encrypted_img:
 encrypted_img.save(r"C:\path\to\your\encrypted_image.jpg")

 decrypted_img = decrypt_image(encrypted_img, secret_key)
 if decrypted_img:
 decrypted_img.save(r"C:\path\to\your\decrypted_image.jpg")




