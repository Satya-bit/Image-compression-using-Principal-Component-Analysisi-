# Image-compression-using-Principal-Component-Analysis-
The project asks the user to upload the image to be compressed. The image is compressed with the help of Principal Component Analysis. 

**=>Introduction**

* Image compression is done to reduce the size of the original image file without degrading the quality of image.


* Image compression will be done using Principal Component Analysis. 


* PCA finds patterns in the data and compresses the data (i.e. dimensionality reduction) with preserving most of the information.


* The concepts of Linear Algebra which are used in PCA are Mean, Standard deviation, Covariance, transpose, Eigenvalue and Eigenvectors for matrix.

**=> How PCA is used**

* PCA approaches the components that are more significant in maintaining the image quality without disturbing the original image quality and minimize the components that are causing image to be larger in size.

* In the image used, PCA is finding the directions of maximum variance in high-dimensional data and project it onto a smaller dimensional subspace while retaining most of the information from that image.

**=> Block Diagram**

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/d13e5a06-2c64-49de-b2c2-784e617b1473)

**=> Workflow**

**=> Step-1** In the first step I covert my image to grayscale. Grayscale only includes luminance(brightness) information and no color information.

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/447c9e61-81d6-4b90-acf6-39ae7e8cbc71)

**=> Step-2** Then the grayscale image is converted into a D*N dimensional matrix(Our code works only for N x N dimensional image.)

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/03b8cef4-4275-4803-bc64-1171e7083a5d)

**=> Step-3** Then we calculated mean of all columns from that matrix
X(mean) = [ X1(mean) X2(mean) X3(mean) …… XN(mean) ] and subtract mean columns from respective columns.

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/220050c3-bd21-484d-87bf-04018829472c)

**=> Step-4** Then we find covariance matrix S for centered data 

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/e0e87ef4-c4c0-4a26-bcb3-70b05b9e4cf5)

**=> Step-5** Then finding Eigen values lambda and Eigen vectors b using QR decomposition algorithm in our code.

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/9430cdc0-d974-40c4-a2b8-478485498718)

**=> Step-6** Sorting Eigen vectors by corresponding Eigen values in descending order

**=> Step-7** Then we are asking user to input the number of principal components M according to user’s need.

**=> Step-8** Then we form matrix B from M(M<D) Eigen vectors and perform dimensionality reduction

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/a2b9e684-e797-47af-a45c-d9646e9b219b)

**=> Step-9** For inverse transformation we need to get back to original space(find projections) and shift data back from the center adding mean values:

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/49e0e6f6-0ec8-4466-a728-afc6cdcb456e)


**=> Results**

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/177e44e5-4c05-40b6-bfbd-0091f70bca91)

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/ec5e0127-0d4a-4dcc-9ec4-18b9a5d9461c)

**=> Conclusions**

![image](https://github.com/Satya-bit/Image-compression-using-Principal-Component-Analysisi-/assets/70309925/f449d6fa-eb54-412c-a75a-3348f01766bf)
