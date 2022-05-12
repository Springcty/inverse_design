"Training Deep Neural Networks for the Inverse Design of Nanophotonic Structures", ACS Photonics 5, 4, 1365-1369 (2018).
Author: Dianjing Liu, Yixuan Tan, Erfan Khoram and Zongfu Yu

This is the implementation of the tandem neural network introduced in the article. 
To reproduce the 2D deisgn result, run the code with ___mode='FNN'___ to __train the forward network__. Then run the code again with ___mode='tandem'___.__# inverse_design__
 
Data set:

There are __600k instances__ in the training data and __5k instances__ in the test data. Both data files are N-by-18 matrices. Each row in the matrices is a training/test instance. The first 9 elements in each row are the input variables listed in Table 2 of the article: d1 x1 w1 d2 x2 w2 d3 x3 w3. The next 3 elements are the following 3 variables:

y1 = 400nm - x1 - w1,

y2 = 400nm - x2 - w2,

y3 = 400nm - x3 - w3.

Since they are duplicate with xi and wi (i=1,2,3), we do not use these 3 variables. The last 6 elements in each row corresponds to the labels. The design parameters in this task are (phi_R, phi_G, phi_B). The last 6 elements are sin(phi_R), sin(phi_G), sin(phi_B), cos(phi_R), cos(phi_G), cos(phi_B).
