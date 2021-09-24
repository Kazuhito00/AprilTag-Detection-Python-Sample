[[Japanese](https://github.com/Kazuhito00/AprilTag-Detection-Python-Sample)/English]

# AprilTag-Detection-Python-Sample
[AprilTag](https://april.eecs.umich.edu/software/apriltag) detection sample in Python.<br>
I use [pupil-labs/apriltags](https://github.com/pupil-labs/apriltags) for detection.<br>
※For environments other than Windows, you can use [AprilRobotics/apriltag](https://github.com/AprilRobotics/apriltag) or [duckietown/lib-dt-apriltags](https://github.com/duckietown/lib-dt-apriltags).

https://user-images.githubusercontent.com/37477845/134534255-85189b37-e89b-44fb-9486-80153df037cf.mp4

# Requirement 
* opencv-python 4.5.3.56 or later
* pupil-apriltags 1.0.4 or later

pupil-apriltags can be installed with pip.
```bash
pip install pupil-apriltags
```

# Tags
Please obtain the tag image from the following.
* [AprilRobotics/apriltag-imgs](https://github.com/AprilRobotics/apriltag-imgs)
* [rgov/apriltag-pdfs](https://github.com/rgov/apriltag-pdfs)

The PDF version is also stored in the [pdf](https://github.com/Kazuhito00/AprilTag-Detection-Sample/tree/main/pdf) directory.

# Demo
Here's how to run the demo.
```bash
python sample.py
```
* --device<br>
Specifying the camera device number<br>
Default：0
* --width<br>
Width at the time of camera capture<br>
Default：960
* --height<br>
Height at the time of camera capture<br>
Default：540
* --families<br>
Tag family<br>
If you specify more than one, separate them with spaces.<br>
Default：tag36h11
* --nthreads<br>
Number of threads<br>
Default：1
* --quad_decimate<br>
Quad detection to increase speed (decrease accuracy)<br>
Full resolution if 1.0 is specified<br>
Default：2.0
* --quad_sigma<br>
Whether to apply Gaussian blur<br>
The setting value indicates the standard deviation in pixels<br>
Very noisy images may be improved by setting a non-zero value (0.8 etc.)<br>
Default：0.0
* --refine_edges<br>
Whether the edges of each Quad are close to a strong gradient<br>
Default：1
* --decode_sharpening<br>
How sharpen the decoded image is<br>
Default：0.25
* --debug<br>
Whether to save the debug image<br>
Default：0

※See [pupil-labs/apriltags#usage](https://github.com/pupil-labs/apriltags#usage) for details on each option

# Reference
* [AprilTag](https://april.eecs.umich.edu/software/apriltag)
* [pupil-labs/apriltags](https://github.com/pupil-labs/apriltags)

# Author
Kazuhito Takahashi(https://twitter.com/KzhtTkhs)
 
# License 
AprilTag-Detection-Python-Sample is under [MIT License](LICENSE).
