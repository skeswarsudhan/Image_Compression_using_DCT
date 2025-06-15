# JPEG Compression and Decompression using DCT

This project implements a simple JPEG-like image compression and decompression algorithm using Discrete Cosine Transform (DCT) in MATLAB.

## Description

The script reads an input image, converts it to YCbCr color space, extracts the luminance (Y) channel, and applies:

- Block-wise DCT (8x8 blocks)
- Quantization (using a standard quantization matrix similar to JPEG)
- Dequantization
- Inverse DCT (IDCT)  
- Finally, it reconstructs the image and saves both the original Y channel and the decompressed image.

## Files

- **Main MATLAB script** (you provided)
- **Input Image**: You need to provide your own image file 
- **Output Images**: The script will save two images:
  - `input3.jpg` (the original Y channel)
  - `output3.jpg` (the decompressed reconstructed image)

## How to Use

1. Open MATLAB.
2. Update the image path in the code:
    ```matlab
    I = imread('C:\Users\S.K.ESWARSUDHAN\Desktop\DSC05582.jpg');
    ```
    Replace it with your own image path.
3. Run the script.
4. After execution, you can find the output images at:
    ```
    C:\Users\S.K.ESWARSUDHAN\Desktop\SK Eswar Sudhan\
    ```
    Replace it with your own path.

## Compression Logic

- The image is divided into 8x8 blocks.
- Each block undergoes DCT.
- Quantization is performed using the `q50` quantization matrix.
- Compressed data is stored.
- For decompression, dequantization and inverse DCT are applied to reconstruct the image.

## Dependencies

- MATLAB (any version that supports basic image processing and matrix operations)
- No external toolboxes are required.

## Notes

- luminance channel (Y) is processed, which simplifies the compression process.
- This code demonstrates the core principle behind JPEG compression.

## Output Example

- You will get compressed and decompressed grayscale images.

## References

- JPEG Compression Standard
- Discrete Cosine Transform
