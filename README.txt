STEGOART IMAGE-TO-IMAGE UPDATE

This update adds automatic secret-image optimization to the existing Image-to-Image module.

How it works:
1. StegoArt first attempts to embed the secret image as a PNG without changing its dimensions or quality.
2. If it does not fit, StegoArt automatically converts it to JPEG, reduces quality, and progressively resizes it until it fits the selected cover image.
3. The decoder detects whether the recovered secret is PNG or JPEG and downloads it with the correct extension.
4. The encoded cover image is still downloaded as PNG. Do not resize, edit, or convert that encoded PNG, because doing so can destroy the hidden data.

Important limitation:
A cover image has finite storage capacity. Automatic optimization removes the need for users to calculate byte limits, but it cannot guarantee that every image will fit every cover image. If the secret image is still too large after optimization, choose a larger cover image.

Steganography hides data; it does not encrypt it.

To publish, replace index.html, style.css, and script.js in the existing GitHub repository, then commit the changes.
