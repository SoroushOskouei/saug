# saug (Space Augmentation)
Space distortions for image augmentations


**Overview**

This Python library provides a collection of functions to apply various distortion effects to images. These effects range from simple pixelation and mirroring to more complex transformations like elastic and wave distortions, enabling creative alterations of images for artistic or experimental purposes. The library leverages NumPy for efficient array manipulations, ensuring high performance even for large images.

**Dependencies**

NumPy: For array operations and mathematical functions.
OpenCV (cv2): For image reading and saving functionalities, as well as some image processing tasks.

**Functions**

This library includes a variety of functions to apply different types of distortions to images. Each function accepts an image (as a NumPy array) as input and returns the distorted image. The main functions include:

elastic_transform: Applies an elastic deformation to the image.

twirl_distortion01 and twirl_distortion02: Apply a twirling effect to parts of the image.

wave_distortion01, wave_distortion02, and wave_distortion: Create wave-like distortions across the image.

pixelate_image: Pixelates a specified region or the entire image.

cartesian_to_polar_image_stretched: Transforms the image from Cartesian to polar coordinates, stretching the pixels.

mirror_effect: Applies a mirroring effect to a specified side of the image.

tilt_shift_effect: Simulates a tilt-shift photography effect, blurring parts of the image while keeping a specific area in focus.

ripple_effect: Creates a ripple effect across the image.

zoom_blur: Applies a zoom blur effect from a specified point.

space_distortion_v1: Distorts the space within the image in a specified direction.

wind_distortion: Simulates the effect of wind on the image.

squeeze_stretch_effect: Applies a squeeze and stretch effect to the image.

smooth_lens_distortion: Applies a smooth lens distortion effect centered around a specified point.

crystallize_distortion: Simulates a crystalline effect by averaging blocks of pixels.

honeycomb_distortion: Applies a honeycomb-like distortion effect across the image.

**Usage Examples**
Below are examples demonstrating how to use some of the functions provided in this library. These examples use a chessboard image as the input, but you can replace it with any image of your choice.


distorted_chessboard = elastic_transform(chessboard, 90, 7)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/0aa6525b-0254-4135-be3c-e8c5294c03bb)

distorted_chessboard = twirl_distortion01(chessboard, (170,270), 200, 0.8)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/66136217-18f5-4599-8efa-1035a09b0cd2)

distorted_chessboard = twirl_distortion02(chessboard, (170,170), 10, 0.12)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/4a8bbc71-7929-4012-a2b2-bfe6ea3aed70)

distorted_chessboard = wave_distortion01(chessboard, (170,100), 10, 10)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/fb19074c-ba98-42e1-905d-f1bb2cf4c761)

distorted_chessboard = wave_distortion02(chessboard, (170,100), 8, 60)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/1738d162-6a85-4d5c-89f9-42fefc03f194)

distorted_chessboard = wave_distortion(chessboard, 8, 80)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/7e9186d5-158a-46ca-9540-4c5bbb26e016)

distorted_chessboard = pixelate_image(chessboard, 14, (50, 50, 340, 340))

![image](https://github.com/SoroushOskouei/saug/assets/57323986/6fe914cc-4ada-4a95-acc3-620b02c4a91d)

distorted_chessboard = cartesian_to_polar_image_stretched(chessboard, center=None)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/a48db0e4-fbd8-4cd7-a00d-dd6ff71ed29c)

distorted_chessboard = mirror_effect(chessboard, direction='horizontal', mirror_line_position=180, side='right')

![image](https://github.com/SoroushOskouei/saug/assets/57323986/3c2735fe-3657-49b1-9a6c-a8f9de95456b)

distorted_chessboard = tilt_shift_effect(chessboard, 0.3, 0.7, 5, 0.4)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/4a36fdc5-889f-4324-b885-e6b3c312478f)

distorted_chessboard = ripple_effect(chessboard, 3, 7)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/54ee2fb8-04c1-4ee4-bad7-46dd67ce85c6)

distorted_chessboard = zoom_blur(chessboard, (150, 150), intensity=0.07, blend=0.3)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/ea101c92-c71f-4019-ba8f-233feb928965)

distorted_chessboard = space_distortion_v1(chessboard)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/ee25c666-bcda-4e2e-9e12-4ac50520c169)

distorted_chessboard = wind_distortion(chessboard, direction=(0.4, -1), strength=21)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/914db25f-4e8f-4115-a191-9dc61d629a32)

distorted_chessboard = squeeze_stretch_effect(chessboard)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/331263b6-7ca1-4a7d-8579-4acd679e7d72)

distorted_chessboard = smooth_lens_distortion(chessboard, 200, 200, 150, 1.3)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/fff13976-7d36-470d-aad1-e70e67a71e4b)

distorted_chessboard = crystallize_distortion(chessboard, crystal_size=27)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/d91b43df-e198-46ea-adee-f9d093f8438a)

distorted_chessboard = honeycomb_distortion(chessboard)

![image](https://github.com/SoroushOskouei/saug/assets/57323986/8dcafd5f-b272-4f8a-aa47-3b93b07e9efd)

