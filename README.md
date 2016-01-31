##-------A example or a test  using webcam to detect  apriltags------------
##--------------Usage--------------------

   Just launch the .launch file
   
```
   $ roslaunch uvc_apriltags_test uvc_apriltags.launch
```
 
   To change the camera device and config, just edit the launch file and yaml file.

   More Usage? Please turn to the  [wiki pages](https://bitbucket.org/HITSZ-NRSL/hitsz_apriltags_ros/wiki/Home) of this repository.

##--------------files --------------------
Include three documents:

**(1)apriltags_ros**

   In this document exists a base apriltag lib and two version of apriltags_ros,now is using **ethz_apriltag2**

   To change the blackborder(default is 1),edit 

   Exmple_of_apriltasgs_from_UVC/apriltags_ros/ethz_apriltag2/include/AprilTags/TagDetector.h

**(2)camera_umd**

   This is an old_uvc camera driver of ros_package
    
**(3)uvc_tast_main**

   This contain a launch file and some init parameter to run the test. 
    
##--------------about dependengces--------------------

Before compling,you shoule add(or install) the dependences as follow:

**1.A old ros package:   uvc_camera**

   see wiki:http://wiki.ros.org/uvc_camera

   source git:   https://github.com/ktossell/camera_umd

**2.Opencv and image_relate dependengce:**

   image_common
   
   image_transport
   
**3.Apriltags_ros (this package include apriltags C++ libraries,that is the leading-role of our test!)**

   http://wiki.ros.org/apriltags_ros----The source code (apriltags C++ libraries) 

   see   http://people.csail.mit.edu/kaess/apriltags/

   ----Infact, the auther of aprtltags is Ed Olson, code Apriltags in java.
   
   see https://april.eecs.umich.edu/wiki/index.php/Download_and_Installation

   https://april.eecs.umich.edu/wiki/index.php/Main_Page

   https://april.eecs.umich.edu/wiki/index.php/AprilTags

   ----Another reference wiki is tekkotsu, see http://wiki.tekkotsu.org/index.php/AprilTags
   
**4.ethz_apriltag2(This is a version of Apriltags_ros edit by ETHZ_ASL team, from kalib)**

  **Notice** This test is using this version. To chuange normal Apriltags_ros, edit the depends of CMakeLists.txt and package.xml before compiling.


