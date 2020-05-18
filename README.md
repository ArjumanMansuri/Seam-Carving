# Seam-Carving
In broad terms, the seam carving algorithm uses horizontal or vertical seams to iteratively reduce the size of the image. A seam is a pixel thick cut through the image that stretches either from left to right or from up to down (depending on the orientation of the seam). Removing the seam reduces the image by one unit. For example, a horizontal seam will reduce the size of the image by one row, and a vertical seam by one column.

The main idea is to find the seams that cut through the non-salient content of the image. In the castle example, we want to generate seams that do not remove details form the castle and the person in the image.

A good seam basically cuts through pixels that are similar with each other. In other words, a good seam is a seam that has small variations in color along the seam. Finding such optimal seams can be done using a dynamic programming algorithm.

The program has 3 arguments: an input image, width of the new target, height of the new target, output image. It retargets the input image to a new image of given sizes and writes it into a file denoted by the last argument. The minimum size of the target image is 2x2 pixels.
Example: ./sc castle.png 300 200 castle2.png
The program (sc) has to generate a new image of size 300x200 that retargets the image in castle.png and saves it in the file castle2.png
