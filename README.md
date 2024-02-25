# Image Generator via Upscaling
This Image Generation approach is similar to Diffusion, 
but it uses Upscaling in the process. 
This is an Experiment using Scikit Learn and in no way better than Stable Diffusion, Dall-E, ...

## Approach
- A video is first converted into thousands of single frames in desired resolutions. *(automatedDataPrep.ipynb)*
- This is then fed to *upscalerGradually.ipynb* which trains a NN on these frames.
  This works by taking the small Resolution Frames as X (Input) and the bigger Resolution Frames as Y (Output).
  In my approach I played around with the hidden layer sizes and found that a single layer with as many neurons as the input shape is quite good.
- The Resulting Models are saved into the specified Folder.
- Testing of the Upscaling Models can be done via *onlyTestingUpscalerGradual.ipynb*

## Results
With my computing power (16GB RAM, i7 QuadCore, No GPU used) it was quite hard to get anything meaningful out of this.
It is interesting to play around with though. If you gave this 10x the Data and hours or days of training, which my system frankly can't handle, 
it would probably actually result in something interesting. I think so because when testing what happens when you give it more or less data,
you can clearly see that more data results in huge improvements. Mhhh, I should try this in the cloud.

###### For my testing until now I only got some more or less blury versions of the input image.
<img width="359" alt="image" src="https://github.com/FelixCodesTech/Image-Generator-via-Upscaling/assets/66774630/181bbec2-e03f-4690-9594-dfb7b6d31987">

###### Some more testing
<img width="345" alt="image" src="https://github.com/FelixCodesTech/Image-Generator-via-Upscaling/assets/66774630/964a3d7b-064e-4f38-b27b-bd1fdfd7bba6">




###### If you use noise for the images, the noise just get's upscaled and you can see some rough contours, but nothing special happens, AFAIK.
<img width="216" alt="image" src="https://github.com/FelixCodesTech/Image-Generator-via-Upscaling/assets/66774630/9cf8e8b4-7fc0-4142-9d02-493cfc43a58c">
