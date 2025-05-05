# cs4277-cs5477-lab1-fun-with-homographies-introduction-solved
**TO GET THIS SOLUTION VISIT:** [CS4277/CS5477 Lab1-Fun with Homographies Introduction Solved](https://www.ankitcodinghub.com/product/cs4277-cs5477-lab1-fun-with-homographies-introduction-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94842&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS4277\/CS5477 Lab1-Fun with Homographies Introduction Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

In this assignment, you will get to implement a panorama stitching algorithm. As discussed in the lectures, images taken using a purely-rotating camera are related by a homography, which can be estimated by at least four point correspondences. You will first implement a homography estimation algorithm, then add a RANSAC scheme to reject outliers. You will also implement a image warping function and use it to stitch together multiple images into a single coherent panorama.

This assignment is worth 15% of the final grade. References: * Lecture 3

Optional references: * HZ Book, Sections 4.1, 4.7, 4.8

Instructions

This workbook provides the instructions for the assignment, and facilitates the running of your code and visualization of the results. For each part of the assignment, you are required to complete the implementations of certain functions in the accompanying python file (lab1.py).

To facilitate implementation and grading, all your work is to be done in that file, and you only have to submit the .py file.

Please note the following:

1. Fill in your name, email, and NUSNET ID at the top of the python file. 2. The parts you need to implement are clearly marked with the following:

<pre>     """ YOUR CODE STARTS HERE """
</pre>
<pre>     """ YOUR CODE ENDS HERE """
</pre>
, and you should write your code in between the above two lines.

3. Note that for each part, there may be certain functions that are prohibited to be used. It is important NOT to use those prohibited functions (or other functions with similar function- ality). If you are unsure whether a particular function is allowed, feel free to ask any of the TAs.

Submission Instructions

Upload your completed lab1.py onto the relevant work bin in Luminus.

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
[2]:

</div>
</div>
<div class="layoutArea">
<div class="column">
Part 1: Homography Estimation from Point Correspondences

In this part, you will implement the Normalized Direct Linear Transformation (DLT) algorithm for homography estimation. This is a linear algorithm for determining the homography transforma- tion H given at least four 2D to 2D point correspondences xi ↔ xi′ (in homogeneous coordinates). The goal is to compute the 3 × 3 homography matrix H such that Hxi = xi′ for each i.

1(a) Transformation using provided homography matrix

To ensure you understand the homography transformation, first implement the function that transform 2D points using a provided homography matrix.

Implement the following function(s): transform_homography() • Prohibited Functions: cv2.perspectiveTransform()

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>input_pts = np.array([[0.0, 0.0], [0.5, 0.0], [1.0, 0.0], [1.0, 0.5],
                      [1.0, 1.0], [0.5, 1.0], [0.0, 1.0], [0.0, 0.5]])
</pre>
<pre>cases = ['translation', 'rigid', 'affine', 'homography']
h = {}
h['translation'] = np.array([[1.0, 0.0, 1.0],
</pre>
<pre>                             [0.0, 1.0, 0.5],
</pre>
<pre>                             [0.0, 0.0, 1.0]])
h['rigid'] = np.array([[0.8660254, -0.5, 0.5],
</pre>
<pre>                       [0.5, 0.8660254, 0.1],
</pre>
<pre>                       [0.0, 0.0, 1.0]])
h['affine'] = np.array([[1.0, 0.5, 0.0],
                        [0.0, 1.5, 0.0],
</pre>
<pre>                        [0.0, 0.0, 1.0]])
h['homography'] = np.array([[1.0, 0.2, 0.0],
</pre>
<pre>                       [0.0, 1.5, 0.0],
                       [0.0, 0.5, 1.0]])
</pre>
<pre>output_pts = {}
for c in cases:
</pre>
<pre>    output_pts[c] = transform_homography(input_pts, h[c])
</pre>
<pre># Print output points and plot
</pre>
<pre>for c in cases:
    print('Points after ({})\n'.format(c), output_pts[c].transpose())
</pre>
<pre>    plt.figure(figsize=(12,5))
    ax = plt.subplot(1, 2, 1)
    ax.axis('equal')
    ax.set(xlim=(-1.0, 3.0), ylim=(-1.0, 3.0))
    plt.title('Before {}'.format(c))
    plt.plot(input_pts[:, 0], input_pts[:, 1], '*')
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>ax = plt.subplot(1, 2, 2)
ax.axis('equal')
ax.set(xlim=(-1.0, 3.0), ylim=(-1.0, 3.0))
plt.title('After {}'.format(c))
plt.plot(output_pts[c][:, 0], output_pts[c][:, 1], '*');
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
You should get the following if the function is implemented correctly:

Points after (translation)

[[1. 1.52. 2. 2. 1.51. 1.] [0.5 0.5 0.5 1. 1.5 1.5 1.5 1. ]]

<pre>Points after (rigid)
 [[0.5      0.933013 1.366025 1.116025 0.866025 0.433013 0.
 [0.1      0.35     0.6      1.033013 1.466025 1.216025 0.966025 0.533013]]
</pre>
<pre>Points after (affine)
 [[0.   0.5  1.   1.25 1.5  1.   0.5  0.25]
 [0.   0.   0.   0.75 1.5  1.5  1.5  0.75]]
</pre>
<pre>Points after (homography)
 [[0.       0.5      1.       0.88     0.8      0.466667 0.133333 0.08    ]
 [0.       0.       0.       0.6      1.       1.       1.       0.6     ]]
</pre>
1(b) Compute Homography Matrix

Now, implement the function to compute the homography matrix given pairs of correspondences using the normalized DLT algorithm.

Implement the following function(s): compute_homography()

• Prohibited Functions: cv2.findHomography(), cv2.getPerspectiveTransform(),

np.linalg.solve(), np.linalg.lstsq()

• You may use the following functions: np.linalg.svd()

Remember to use normalization, which will increase the robustness of the estimation.

</div>
</div>
<div class="layoutArea">
<div class="column">
0.25 ]

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre># Test case with exactly 4 points
</pre>
<pre>src1 = np.array([[0.0, 0.0], [331.0, 0.0], [331.0, 474.0], [0.0, 474.0]])
dst1 = np.array([[182.0, 94.0], [482.0, 48.0], [598.0, 466.0], [146.0, 533.0]])
homo1 = compute_homography(src1, dst1)
</pre>
<pre># Test case with more than 4 points
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[3]:

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>src2 = np.array([[434.375, 93.625], [429.625, 190.625],
                 [533.625, 301.875], [452.375, 460.625],
                 [558.375, 188.625], [342.444, 362.596],
                 [345.625, 41.875], [341.625, 146.125]])
</pre>
<pre>dst2 = np.array([[204.780, 92.367], [201.875, 190.625],
                 [297.125, 296.875], [224.446, 456.556],
                 [318.407, 192.155], [107.625, 371.375],
                 [109.875, 26.624], [106.625, 138.125]])
</pre>
<pre>homo2 = compute_homography(src2, dst2)
</pre>
<pre>print('homo1:\n', homo1, '\n')
print('homo2:\n', homo2)
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
You should obtain approximately the following (or some scale of it) if your function is imple- mented correctly:

<pre>homo1:
 [[ 9.012217e-01 -1.792522e-01  1.820000e+02]
 [-1.394830e-01  5.490343e-01  9.400000e+01]
 [-1.062811e-05 -7.075535e-04  1.000000e+00]]
</pre>
<pre>homo2:
 [[ 1.738142e+00  9.494425e-03 -4.466937e+02]
 [ 2.745643e-01  1.514698e+00 -1.213769e+02]
 [ 1.160079e-03  2.069049e-05  1.000000e+00]]
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
Part 2: Image Warping using Homography

In this part, you will implement the image warping function. Given two images Isrc, Idst and the homography matrix H which relates the coordinates in the two images:

xdst = Hxsrc

, where xsrc and xdst are pixel coordinates of Isrc and Idst respectively, the objective is to warp Isrc

onto Idst.

The obvious way of doing this is forward-interpolation, where for every pixel in Isrc, you compute where it should be in Idst and copy the pixel value over. However this will result in holes in the image (why?).

The better way is to do it in the reverse direction (i.e. backward interpolation), where we com- pute the corresponding coordinate in Isrc for every pixel in Idst. First create a HdstWdst × 2 matrix containing the coordinates of all the pixels in Idst, i.e,

􏰃0 0 0 … Wdst −1 Wdst −1􏰄T 0 1 2 … Hdst−2 Hdst−1 ,

where Wdst and Hdst are the width and height of Idst. Then use your transform_homography() function to compute the corresponding coordinates in Isrc. Lastly, for every pixel in the destination image, fill its value with the corresponding pixel in the source image; you can use interpolation methods to handle non-integer soure pixel coordinates.

Implement the following function(s): warp_image() • Prohibited Functions: cv2.warpPerspective()

• You may use the following functions: cv2.remap(), np.meshgrid()

If you use cv2.remap, you might find the borderMode value of cv2.BORDER_TRANSPARENT useful.

Also consider using bilinear interpolation in cv2.remap.

Let us now use our functions so far to replace the book cover with another image. If all above functions are implemented correctly, you should see the book cover being replaced by another image when you run the following code.

[4]:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
template = load_image(‘data/hzbook_2.jpg’)

original = load_image(‘data/hzbook_1.jpg’)

# homo is the homography matrix that maps points in template to original homo = np.array([[ 9.01221661e-01, -1.79252179e-01, 1.82000000e+02],

<pre>                 [-1.39482959e-01,  5.49034320e-01, 9.40000000e+01],
</pre>
<pre>                 [-1.06281109e-05, -7.07553504e-04, 1.00000000e+00]])
overlaid = warp_image(template, original, homo)
</pre>
<pre>plt.figure()
plt.imshow(template)
plt.title('Template')
plt.figure(figsize=(12,6))
plt.subplot(1,2,1)
plt.imshow(original)
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>plt.title('Original image')
plt.subplot(1,2,2)
plt.imshow(overlaid)
plt.title('Modified image');
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[5]:

</div>
</div>
<div class="layoutArea">
<div class="column">
Part 3: Robust Homography Estimation using RANSAC

In this part, we upgrade our homography estimation algorithm to be robust even in the presence of outliers. Consider the following image stitching example containing 10 provided correspon- dences.

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>im1 = load_image('data/pano_2.jpg')
im2 = load_image('data/pano_3.jpg')
</pre>
<pre>im1_points = np.array([[434.375, 93.625], [429.625, 190.625],
                       [533.625, 301.875], [452.375, 460.625],
                       [558.375, 188.625], [342.444, 362.596],
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
7

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="section">
<div class="layoutArea">
<div class="column">
􏰅→outliers

</div>
</div>
<div class="layoutArea">
<div class="column">
[345.625, 41.875], [341.625, 146.125],

[424.375, 385.375], [602.875, 183.125]]) # last row is␣

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>im2_points = np.array([[204.780, 92.367], [201.875, 190.625],
                       [297.125, 296.875], [224.446, 456.556],
                       [318.407, 192.155], [107.625, 371.375],
</pre>
[109.875, 26.624], [106.625, 138.125],

[514.526, 142.354], [348.375, 304.375]]) # last row is␣

􏰅→outliers

vis = draw_matches(im1, im2, im1_points, im2_points)

<pre>plt.figure(figsize=(16, 8))
plt.imshow(vis);
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
8

</div>
</div>
</div>
<div class="page" title="Page 9">
<div class="layoutArea">
<div class="column">
Notice that 2 of the 10 correspondences are wrong. Using just the correct correspondences yields the correct result:

[6]:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
im1_points_inliers = im1_points[:-2, :] # exclude the last 2 wrong␣ 􏰅→correspondences

<pre>im2_points_inliers = im2_points[:-2, :]
homo = compute_homography(im1_points_inliers, im2_points_inliers)
</pre>
<pre>stitched = warp_images_all([im1, im2], [homo, np.eye(3)])
plt.figure(figsize=(12, 8))
plt.imshow(stitched)
</pre>
<pre>print('Computed homography matrix:\n', homo)
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[7]:

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>Computed homography matrix:
 [[ 1.738142e+00  9.494425e-03 -4.466937e+02]
 [ 2.745643e-01  1.514698e+00 -1.213769e+02]
 [ 1.160079e-03  2.069049e-05  1.000000e+00]]
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
However, if we include the two outliers, notice that the alignment fails.

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>homo = compute_homography(im1_points, im2_points)
</pre>
<pre>stitched = warp_images_all([im2, im1], [np.eye(3), homo])
plt.figure(figsize=(12, 8))
plt.imshow(stitched);
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
9

</div>
</div>
</div>
<div class="page" title="Page 10">
<div class="layoutArea">
<div class="column">
The de-facto algorithm to solve this is RANdom SAmple Consensus (RANSAC). Your task is now to implement the robust homography computation which can handle outliers. RANSAC requires a error distance function to compute which correspondences are outliers. First, implement the symmetric transfer error distance measure as described in the lectures:

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰂 􏰂2 􏰂 􏰂 ′ 􏰂 −1′􏰂 ′ 2

</div>
</div>
<div class="layoutArea">
<div class="column">
d(x,x;H)=􏰂x−H x􏰂 +􏰂x −Hx􏰂 .

</div>
</div>
<div class="layoutArea">
<div class="column">
Implement the following function(s): compute_homography_error()

• Prohibited Functions: cv2.findHomography()

• You may use the following functions: np.linalg.inv(), and transform_homography() from the previous sections.

[8]:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>src = np.array([[0.0, 0.0], [1.0, 0.0], [2.0, 1.0]])
dst = np.array([[1.0, 2.0], [1.5, 2.5], [2.5, 3]])
H = np.array([[0.5, 0.0, 1.0],
</pre>
<pre>              [0.0, 0.5, 2.0],
              [0.0, 0.0, 1.0]])
</pre>
<pre>print('Error:', compute_homography_error(src, dst, H))
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
If implemented correctly, the previous code should print:

<pre>    Error: [0.   1.25 2.5 ]
</pre>
Now implement the RANSAC procedure covered in the lectures, using the error distance measure you just implemented:

Be sure to re-estimate the homography transformation using all the inliers at the end of the RANSAC procedure.

</div>
</div>
<div class="layoutArea">
<div class="column">
10

</div>
</div>
</div>
<div class="page" title="Page 11">
<div class="layoutArea">
<div class="column">
Implement the following function(s): compute_homography_ransac()

• Prohibited Functions: cv2.findHomography()

• You may use the following functions: compute_homography() function from the previous

sections.

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>homo, mask = compute_homography_ransac(im1_points, im2_points)
stitched = warp_images_all([im1, im2], [homo, np.eye(3)])
</pre>
<pre>plt.figure(figsize=(12, 8))
plt.imshow(stitched)
</pre>
<pre>vis = draw_matches(im1, im2, im1_points, im2_points, inlier_mask=mask)
plt.figure(figsize=(16, 8))
plt.imshow(vis)
</pre>
<pre>print('Computed homography matrix:\n', homo)
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[8]:

</div>
</div>
<div class="layoutArea">
<div class="column">
11

</div>
</div>
</div>
<div class="page" title="Page 12">
<div class="layoutArea">
<div class="column">
If you implemented the above correctly, the above images should be aligned correctly. The RANSAC algorithm detects outliers (drawn in red) and excludes them from the homography computation. The computed homography matrix should be the same as the previous sections:

<pre>      [[ 1.738142e+00  9.494425e-03 -4.466937e+02]
      [ 2.745643e-01  1.514698e+00 -1.213769e+02]
      [ 1.160079e-03  2.069049e-05  1.000000e+00]]
</pre>
At this point, we now can perform automatic alignment of the image pair. Recall in the lectures that we can detect keypoints and match them between the two images. The matches generally will contain outliers but your robust homography computation can handle those and still output the correct homography.

Let’s see how our algorithm performs in such a scenario.

First, let us use OpenCV’s feature detection, extraction and matching pipeline to establish poten- tial correspondences in the two images.

[9]:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre># Initiate ORB detector. Detect keypoints and extracts descriptors with ORB
</pre>
<pre>orb = cv2.ORB_create()
kp1, des1 = orb.detectAndCompute(cv2.cvtColor(im1, cv2.COLOR_BGR2GRAY), None)
kp2, des2 = orb.detectAndCompute(cv2.cvtColor(im2, cv2.COLOR_BGR2GRAY), None)
</pre>
<pre># Matches the descriptors via brute force matching
</pre>
<pre>bf = cv2.BFMatcher(cv2.NORM_HAMMING, crossCheck=True)
matches = bf.match(des1,des2)
im1_points_orb, im2_points_orb = matches2pairs(matches, kp1, kp2)
</pre>
<pre>vis = draw_matches(im1, im2, im1_points_orb, im2_points_orb)
plt.figure(figsize=(16, 8))
plt.imshow(vis);
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
We can see that some of the correspondences are wrong. So how does our compute_homography_ransac() function perform?

</div>
</div>
<div class="layoutArea">
<div class="column">
12

</div>
</div>
</div>
<div class="page" title="Page 13">
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>homo, mask = compute_homography_ransac(im1_points_orb, im2_points_orb)
stitched = warp_images_all([im1, im2], [homo, np.eye(3)])
</pre>
<pre>plt.figure(figsize=(12, 8))
plt.imshow(stitched)
</pre>
<pre>vis = draw_matches(im1, im2, im1_points_orb, im2_points_orb, inlier_mask=mask)
plt.figure(figsize=(16, 8))
plt.imshow(vis);
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[10]:

</div>
</div>
<div class="layoutArea">
<div class="column">
If implemented correctly, the images should be aligned properly, with the inliers and outliers correctly detected.

</div>
</div>
<div class="layoutArea">
<div class="column">
13

</div>
</div>
</div>
<div class="page" title="Page 14">
<div class="layoutArea">
<div class="column">
Part 4: Adding more images

You are almost done! Now the last part is to extend the stitching to multiple images. To do so, suppose we have N images I1, . . . , IN. We perform pairwise matching between consecutive images (i.e. I1 → I2, I2 → I3, . . .). We can then set one of the images (e.g. middle one) as the reference image, and warp all the homographies to it.

Implement the function that computes the homography warping matrices for each image from pairwise homography matrices. Specifically, given H21, H32, . . . , HN−1 which represents the ho- mography matrices between consecutive images:

</div>
</div>
<div class="layoutArea">
<div class="column">
xk+1 = Hk+1xk, k

compute the absolute homography matrices Hre f , Hre f , . . . , Hre f

</div>
<div class="column">
that can be used to warp all im-

</div>
</div>
<div class="layoutArea">
<div class="column">
1 2 N−1 Implement the following function(s): concatenate_homographies()

</div>
</div>
<div class="layoutArea">
<div class="column">
ages to the reference image:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
# Initiate ORB detector. Detect keypoints and extracts descriptors for all␣ 􏰅→images.

<pre>orb = cv2.ORB_create()
num_images = 4
all_im, all_kp, all_des = [], [], []
for i in range(num_images):
</pre>
<pre>    im = load_image('data/pano_{}.jpg'.format(i))
    kp, des = orb.detectAndCompute(cv2.cvtColor(im, cv2.COLOR_BGR2GRAY), None)
    all_im.append(im)
    all_kp.append(kp)
    all_des.append(des)
</pre>
# Matches the descriptors between consecutive images via brute force matching,␣ 􏰅→and

<pre># computes the homography matrices.
</pre>
<pre>bf = cv2.BFMatcher(cv2.NORM_HAMMING, crossCheck=True)
pairwise_homographies = []
for i in range(num_images-1):
</pre>
<pre>    matches = bf.match(all_des[i], all_des[i+1])
</pre>
im1_points_orb, im2_points_orb = matches2pairs(matches, all_kp[i],␣ 􏰅→all_kp[i+1])

<pre>    h_i1_i, mask = compute_homography_ransac(im1_points_orb, im2_points_orb)
    pairwise_homographies.append(h_i1_i)
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[11]:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
<pre>all_h_matrices = concatenate_homographies(pairwise_homographies, ref=2)
</pre>
<pre>stitched = warp_images_all(all_im, all_h_matrices)
plt.figure(figsize=(16, 8))
plt.imshow(stitched);
</pre>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
[12]:

</div>
</div>
<div class="layoutArea">
<div class="column">
14

</div>
</div>
</div>
<div class="page" title="Page 15">
<div class="layoutArea">
<div class="column">
If you implemented concatenate_homographies() correctly, you should get a coherent panorama. Congratulations! You have reached the end of the first assignment.

</div>
</div>
<div class="layoutArea">
<div class="column">
15

</div>
</div>
</div>
