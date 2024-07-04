# PixelDust - a CLI based Image Encryption 

PixelDust is a command-line tool for encrypting and decrypting images using XOR encryption. It supports both encryption and decryption of images with a randomly generated key.

## Features

- Encrypt images using XOR encryption.
- Decrypt images using the provided key.
- Supports custom output file names for both encrypted images and keys.
- Suported formats: `png`, `jpg` and `jpeg`.

## Dependencies

- npm
- Node.js

## Installation

To use pixelDust, you need to have Node.js installed. Then, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/AvijeetJain/pixelDust.git
    ```

2. Navigate to the project directory:
    ```bash
    cd pixelDust
    ```

3. Install the dependencies:
    ```bash
    npm install
    ```
## Commands Available

List of all the command available:

```sh
  -h, --help                 # Lists all avalibe commands
  -e, --encrypt              # The image to encrypt
  -d, --decrypt              # The image to decrypt
  -c, --clear                # Clear the console Default: false
  --noClear                  # Don't clear the console Default: true
  -v, --version              # Print CLI version Default: false
  -k, --key                  # The key to use for decryption Default: false
  -i, --outputImageFileName  # The output image
  -p, --outputKeyFileName    # The output key
```

## Usage

### Encrypt an Image

To encrypt an image, use the following command:

```bash
pixeldust --encrypt <image_path> --outputImageFileName <output_image> --outputKeyFileName <key_file>
```

### Decrypt an Image

To decrypt an image, use the following command:

```bash
pixeldust --decrypt <encrypted_image_path> --key <key_file> --outputImageFileName <decrypted_image>
```

## Limitation

While encryption and decryption of PNG images are flawless, the process encounters challenges with JPG and JPEG formats. These formats employ lossy compression, which discards some image data to reduce file size and introduces compression artifacts. Additionally, they undergo color space conversion and quantization during compression, affecting pixel precision. Moreover, their block-based compression method can cause blocky artifacts, which may become more noticeable after decryption. Consequently, decrypted JPG and JPEG images exhibit minor differences in pixel values compared to the original.

## Contributing

Feel free to open issues or contribute to the project. Pull requests are always welcomed.
