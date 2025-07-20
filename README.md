Using scharr filter to approximate gradient difference in horizontal and vertical direcitons . To apply this filter we do convolution operations with 3x3 matrix .

For X direction : [-3 0 3; -10 0 10; -3 0 3]
For Y direction : [3 10 3; 0 0 0; -3 -10 -3]
then we combine results of 2 convolution(X and Y) ; MAgnitude = sqrt(X^2 + Y^2).

Using these filters we extract the edges where sudden change is happening and then we can optionaly use the dilate mask function of opencv to get complete object in the mask.


<img width="618" height="443" alt="bird" src="https://github.com/user-attachments/assets/8366b0b4-0f0a-4e79-82ac-a43fa8116f92" />

You can tune parameters like threshold and dilation iterations and may morphology funcitions of opencv to get even better results.



I have tried to keep the code as simple as possible. The code has less than 20 lines. It uses simple mathematical funcitons to achieve this result.
