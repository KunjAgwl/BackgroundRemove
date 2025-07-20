Using scharr filter to approximate gradient difference in horizontal and vertical direcitons . To apply this filter we do convolution operations with 3x3 matrix .
For X direction : [-3 0 3; -10 0 10; -3 0 3]
For Y direction : [3 10 3; 0 0 0; -3 -10 -3]
then we combine results of 2 convolution(X and Y) ; MAgnitude = sqrt(X^2 + Y^2).

Using these filters we extract the edges where sudden change is happening and then we can optionaly use the dilate mask function of opencv to get complete object in the mask.
