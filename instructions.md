## Tips if you are not getting expected results:

1. If you are getting an error, try an image with a smaller resolution.
2. If you are trying out images of humans, especially faces, note that it is unfortunately not the intended use case. We would encourage trying out images of everyday objects instead, or even artworks.
3. If some part of the object is missing, check the 3D interactive camera angle visualization pane (top right) where you can find the input image actually used for the model after the automatic preprocessing steps, and verify whether the segmented image contains the entire object you are trying to rotate.
4. The model is probabilistic, therefore if the number of samples is selected to be bigger than 1 and results look different, that is expected behavior as the model tries to predict a diverse set of possibilities given the input image and the specified camera viewpoint.
5. Under "advanced options", you can tune two parameters as you can typically find in other diffusion model demos as well:
	- Diffusion Guidance Scale defines how much you want the model to respect the input information (image + angles). Higher scale typically leads to less diversity and higher image distortion.
	- Number of diffusion inference steps controls the number of denoising iterations that are applied in order to generate each image. Usually the higher the better (with potentially diminishing returns).

Have fun! :smiley:

A model card can be found here: [uses.md](https://github.com/cvlab-columbia/zero123/blob/main/zero123/uses.md)