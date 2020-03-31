# Computer-Vision-Image-Blending
Image blending Image pyramids are image representations useful for many downstream applications. This problem uses pyramid image processing to blend two images.


(a) As a first step, implement functions pyr up, pyr down, gaussian pyramid, laplacian pyramid,
reconstruct img to build a Laplacian pyramid from one image and show that you can reconstruct back the original image. Please use Gaussian kernels with the same size for pyr up and
pyr down. The only difference is that the kernel for pyr up will be the one used for pyr down
multiplied by 4. Please plot the original image, the Laplacian pyramid, and the reconstructed
image. Please use a Laplacian pyramid with 4 levels. (Hint: np.insert may come in handy
when implementing pyr up) (4 points)

(b) Implement functions pyr blend(im1, im2, mask, num levels) that takes as input two
images and a binary mask (indicating which pixels to use from each image) and produces the
Laplacian pyramids with num levels levels for blending the two images. Use your function
to blend the orange and apple image we provide in the Colab notebook. Plot the blended
images with num levels ∈ {1, 2, 3, 4, 5, 6}. Please describe the difference between the blended
images with different levels of Laplacian pyramid: how does the result change as you use more
pyramid levels?

To obtain color images, you can apply the blending to each color channel independently. In
our implementation, this did not require any extra code (the same code worked on singlechannel and multi-channel images due to numpy broadcasting), but your implementation may
differ. (2 points)
