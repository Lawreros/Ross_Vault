name : Peak signal-to-noise ratio (PSNR)
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Peak_signal-to-noise_ratio

###### Content:
The peak signal-to-noise ration is the ration between the maximum possible power of a signal and the power of corrupting noise. It is commonly used to quantify reconstruction quality for images and video subject to [[lossy compression]]. Because many signals have a very wide dynamic range, PSNR is usually expressed as a logarithmic quantity using the decibel scale.

PSNR is most easily defined via the [[mean squared error]]. Given a noise-free $m\times n$ monochorme image $I$ and its noisy approximation $K$:
$$MSE = \frac{1}{mn}\sum_{i=0}^{m-1}\sum_{j=0}^{n-1}|I(i,j)-K(i,j)|^2$$
The PSNR in decibles is defined as:
$$PSNR = 10 \cdot log_{10}(\frac{MAX_I^2}{MSE})
=20 \cdot log_{10}(MAX_I) - 10\cdot log_{10}(MSE)$$
where $MAX_I$ is the maximum possible pixel value of the image. When the pixels are represented using 8 bits per sample, this is 255.

###### Properties:
- When calculating PSNR for color images, the definition is the same except that the MSE is the sum over all squared value differences (for each color) divided by the image size and by the number of color channels.
- Generally, the higher the PSNR, the better the reconstruction. However this is not always the case, as the higher PSNR image may look worse to the human eye. It is wise to also check with other methods: https://en.wikipedia.org/wiki/Video_quality

###### Additional Thoughts:
