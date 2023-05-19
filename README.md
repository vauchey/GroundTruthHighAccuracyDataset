
# Particle filter meets hybrid octrees: an octree-based vehicle localization approach without learning (Submitted by [ESIGELEC](https://www.esigelec.fr/))

## News :
* 2023/05/20 : Full dataset is availaible here : [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7951627.svg)](https://doi.org/10.5281/zenodo.7951627)

* 2023/01/14 : Add off-road datasets [here](#OFFROAD)

* 2022/12/15 : Update dataset directories

* 2020/07/17 : A new dataset is availaible  [here](#JULY) on same road than previous.

* 2020/06/18 : A new dataset is availaible  [here](#JUNE) on same road than previous.

* 2020/05/15 : A new dataset is availaible  [here](#MAY) on same road than previous.

* April 2020 : Due to the COVID19, no dataset were done in appril.

* 2020/03/17 : A second dataset is availaible  [here](#MARCH) on same road than previous.

* 2020/02/18 : A first dataset is availaible (dataset used for paper) [here](#FEBRUARY).

## Abstract :
This paper proposes an accurate lidar-based outdoor localization method that requires few computational resources, is robust in challenging environments (urban, off-road, seasonal variations) and whose performances are equivalent for two different sensor technologies: scanning LiDAR and flash LiDAR. The method is based on the matching between a pre-built 3D map and the LiDAR measurements. Our contribution lies in the combined use of a particle filter with a hybrid octree to reduce the memory footprint of the map and significantly decrease the computational load for online localization. The design of the algorithm allows it to run on both CPU and GPU with equivalent performance. We have evaluated our approach on the KITTI dataset and obtained good results compared to the state of the art. This paper introduces the baseline performance on a multi-seasonal dataset we are publicly releasing to the community. We have shown that the same localization algorithms and parameters can perform well in urban environments and can be extended to off-road environments. We have also evaluated the robustness of our method when masking angular sectors of the LiDAR field of view to reproduce edge-cases scenarios in urban environments where the LiDAR field is partially occulted by another vehicle (bus, truck). Finally, experiments have been carried out with two distinctive scanning and flash LiDAR technologies. The performance achieved with the flash LiDAR is close to the scanning LiDAR despite different resolutions and sensing modalities. The positioning performance is significant with 10cm and 0.12° angular RMSE for both technologies. We validated our approach in an off-road environment from a front view field of view with only 768 LiDAR points.



[![](https://img.youtube.com/vi/BLnmOXnFlSA/0.jpg)](https://www.youtube.com/watch?v=BLnmOXnFlSA)

Vincent VAUCHEY¹⁴, Pierre MERRIAUX², Xavier SAVATIER³, Yohan DUPUIS⁴.  
¹[ESIGELEC](http://www.esigelec.fr/) , IRSEEM, Rouen, France, Normandie Univ, UNIROUEN, 
²[Leddartech](http://www.leddartech.com.),   Quebec   City,   Canada 
³[ESIGELEC](https://navya.tech/fr/) , NAVYA, Paris, France
⁴[CESI](http://www.cesi.fr/) , CESI, La Défense, Paris, France, 



vvauchey@cesi.fr
pierre.merriaux@leddartech.com
xavier.savatier@navya.tech
ydupuis@cesi.fr
fourre@esigelec.fr

Special Thanks to the members of the [SIRD](http://www.esigelec.fr/en/node/113) team : Marc DEHAIS, Anthony DESHAIS, Christophe ALEGRE, Pascal FALLA, Jérémy FOURRE
# Datasets
Dataset Lidar/IMU/RGBD Camera done by Vincent VAUCHEY.


[![](https://img.youtube.com/vi/6mwToyNoxMQ/0.jpg)](https://www.youtube.com/watch?v=6mwToyNoxMQ)

The main reference dataset for lidar localisation is [KITTY](http://www.cvlibs.net/datasets/kitti/) dataset and is used for a lot of paper and result comparaisons beetweens localization/SLAM algorithms. The main difficultiy to use [KITTY](http://www.cvlibs.net/datasets/kitti/) dataset is the ground true accuracy which is many times more than 20 cm.

We try to provide to the community some datasets done with a reference position with best positioning systems avaiblaibles in all conditions.
The datasets ground True is done with a Landyns ([IXblue](https://www.ixblue.com/)) IMU based on fiber-optic-gyroscope (FOG), which is a technology wich ensure very low shift and noise between two gps position or when the gps accurancy become low.
In addition of this very high accurate IMU, we're also using a postprocessing application ([APPS](https://www.ixblue.com/products/apps)) coupled whith a GPS RTK [septentrio](https://www.septentrio.com/) . The goal of this application is to increase the accuracy of ground true position especially when there is tree/tunnel by doing forward/backward Kallman Filter. Landyn IMU is an "old" IMU without new firmware release but with better FOG than IMU currently in sale for civil application by [IXblue](https://www.ixblue.com/). The fact to use APPS software give the possibility to use processing algorithms used on the last IMU in sale by ([IXblue](https://www.ixblue.com/)) on our Landyn.

## IMU COMPARAISON :
| IMU  | LANDYN ([IXblue](https://www.ixblue.com/))        | ATLANS ([IXblue](https://www.ixblue.com/))  | RT 3000 ([Oxts](https://www.oxts.com/))
| :--------------- |:---------------:|:---------------:|:---------------:|
| Position when RTK lost (m)  | 0.20 (GNSS outage 60s) | 0.350 (GNSS outage 60s)  |  1.5 (SPS)
| Pitch/Roll (deg)  | 0.005 (RTK) / 0.005 (GNSS outage 60s) | 0.008 (RTK) / 0.01 (GNSS outage 60s) | 0.03
| Heading (deg)  | 0.01 | 0.020 | 0.1




<a id="FEBRUARY"></a>
#### DATASET 2020/02/18 : 
* Loop1 : Winter sun and some clouds (~1.5km)

    * [30 km/h dataset A (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP1_30kmA.zip?download=1)
    * [30 km/h dataset B (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP1_30kmB.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP1_40km.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP1_50km.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [![](images/LOOP1.gif)](https://www.google.com/maps/d/embed?mid=1cAdJnWjBnK7ZZkCva8ftSXN_qYLh2o9t   )

    [maps preview](https://www.google.com/maps/d/embed?mid=1cAdJnWjBnK7ZZkCva8ftSXN_qYLh2o9t)
    
    


        

* Loop2 : Winter sun and some clouds with one short tunnel (~2.6 km)

    * [30 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP2_30km.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP2_40km.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_02_18_LOOP2_50km.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [![](images/LOOP2.gif)](https://www.google.com/maps/d/embed?mid=1aRvGyCyWWRs2k5G5HH2M6DCKO5p3p3LA)

    [maps preview](https://www.google.com/maps/d/embed?mid=1aRvGyCyWWRs2k5G5HH2M6DCKO5p3p3LA)



<a id="MARCH"></a>
#### DATASET 2020/03/17 :
Images will be availaible as soon as the containment due to the COVID19 will be finish.

* Loop1 : Winter sun (~1.5km)
    * [30 km/h dataset A (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP1_30KMH_A.zip?download=1)
    * [30 km/h dataset B (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP1_30KMH_B.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP1_40KMH.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP1_50KMH.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [![](images/LOOP1_March.gif)](https://www.google.com/maps/d/embed?mid=1cAdJnWjBnK7ZZkCva8ftSXN_qYLh2o9t   )

* Loop2 : Winter sun  (~2.6 km) {: #funky }

    * [30 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP2_30KMH.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP2_40KMH.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_03_17_LOOP2_50KMH.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [![](images/LOOP2_March.gif)](https://www.google.com/maps/d/embed?mid=1aRvGyCyWWRs2k5G5HH2M6DCKO5p3p3LA)

<a id="MAY"></a>
#### DATASET 2020/05/15 : 
* Loop1 : spring (~1.5km)

    * [30 km/h dataset A (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP1_30KMH_A.zip?download=1)
    * [30 km/h dataset B (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP1_30KMH_B.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP1_40KMH.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP1_50KMH.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [maps preview](https://www.google.com/maps/d/embed?mid=1cAdJnWjBnK7ZZkCva8ftSXN_qYLh2o9t)
    Now no camera dataset will done due to the big amouth of data generated and the few interests of this kind of dataset.
* Loop2 :  spring (~1.5km)

    * [30 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP2_30KMH.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP2_40KMH.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_05_15_LOOP2_50KMH.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [maps preview](https://www.google.com/maps/d/embed?mid=1aRvGyCyWWRs2k5G5HH2M6DCKO5p3p3LA)
    Now no camera dataset will done due to the big amouth of data generated and the few interests of this kind of dataset.

<a id="JUNE"></a>
#### DATASET 2020/06/18 : 
* Loop1 : spring (~1.5km)
    * [30 km/h dataset A (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP1_30KMH_A.zip?download=1)
    * [30 km/h dataset B (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP1_30KMH_B.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP1_40KMH.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP1_50KMH.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [maps preview](https://www.google.com/maps/d/embed?mid=1cAdJnWjBnK7ZZkCva8ftSXN_qYLh2o9t)

* Loop2 :  spring (~1.5km)

    * [30 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP2_30KMH.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP2_40KMH.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_06_18_LOOP2_50KMH.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [maps preview](https://www.google.com/maps/d/embed?mid=1aRvGyCyWWRs2k5G5HH2M6DCKO5p3p3LA)

<a id="JULY"></a>
#### DATASET 2020/07/17 :
* Loop1 : spring (~1.5km)
    * [30 km/h dataset A (Download)](https://zenodo.org/record/7951627/files/2020_07_17_LOOP1_30kmA.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_07_17_LOOP1_40km.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_07_17_LOOP1_50km.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [maps preview](https://www.google.com/maps/d/embed?mid=1cAdJnWjBnK7ZZkCva8ftSXN_qYLh2o9t)

* Loop2 :  spring (~1.5km)

    * [30 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_07_17_LOOP2_30kmA.zip?download=1)
    * [40 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_07_17_LOOP2_40km.zip?download=1)
    * [50 km/h dataset (Download)](https://zenodo.org/record/7951627/files/2020_07_17_LOOP2_50km.zip?download=1)
    * [Directory Tree and calibrations](#TREE)

    [maps preview](https://www.google.com/maps/d/embed?mid=1aRvGyCyWWRs2k5G5HH2M6DCKO5p3p3LA)


<a id="OFFROAD"></a>
#### DATASET offroad :
* Datasets off road (no pic availaibles becase done on a private area)

    * [Falling1 (Download)](https://zenodo.org/record/7951627/files/2020_11_23Falling1.zip?download=1)

    * [Falling2 (Download)](https://zenodo.org/record/7951627/files/2020_11_23falling2.zip?download=1)

    * [Rising2 (Download)](https://zenodo.org/record/7951627/files/2020_11_23Rising2.zip?download=1)

    * [Rising3  (Download)](https://zenodo.org/record/7951627/files/2020_11_23Rising3.zip?download=1)

    * [Directory Tree and calibrations](#TREE)
    [maps preview](https://www.google.com/maps/d/edit?mid=1LSxdVwQbkd-xmMvE0Gxr--NR1REUOr8)

List of sensors and software used :
* vlp16 Lidar synchronised on GPS ([Velodyne](https://velodynelidar.com/))
* GPS AsterRx-U ([septentrio](https://www.septentrio.com/))
* LANDYN IMU + post processing software APPS ([IXblue](https://www.ixblue.com/))
* D435 trigged on IMU ([intelrealsense](https://www.intelrealsense.com/depth-camera-d435))
* Peiseler odometer mounted on the right rear wheel.
* RTMAPS ([Intempora](https://intempora.com/)) Realtime acquisition software (can also be used to replay datasets)
* Rtk correction network ([teria](https://www.reseau-teria.com/reseau/)) 
* PCAN-USB ([peak-system](https://www.peak-system.com)) 

![](images/espace1.jpg )

<a id="TREE"></a>

Directory Tree :
* lidarCorrectedSynchronisedImuPostPro.zip : lidar corrected  + imu + postpro synchronised
* lidarUnCompensatedImuPostProUnsynchronised : lidar uncorrected + imu + postpro unsynchronised (Download)
* vehicleOdometry : vehicle longitudinal speed (m/s) and can yaw rate (r/s) timestamped but not calibrated.

<span style="color:red">Due to European Union RGPD limitation, images were removed.</span>

Calibrations (X forward, Y left, Z Up) :
* Transformation IMU to Lidar (Tx,Ty,Tz,Rx,Ry,Rz) : [0.989,-0.024, 2.388,0.0,0.0,-0.385]
* Car odometry and IMU have the same measurement points (rear axle)
* Transformation lidar to rgbd Camera (Tx,Ty,Tz,Rx,Ry,Rz) : [0.74,-0.43, 0.0,0.0,0.0,0.0], python code to read XYZ png file is availaible [here](code/convertionImageXYZto3D.py)
* Camera intrinsic calibration availaible [here](https://esigelec-my.sharepoint.com/:t:/g/personal/fourre_esigelec_fr/EUoTHjIptlZFvK3sz9gQn0UBtUI7xqMdJq1leUGLj6U6wQ?e=EbRiLk)
### Context :
The dataset localization are datasets on same road than the French Project "Rouen Normandy Autonomous Lab" with Renault and Transdev partners:

[![](https://img.youtube.com/vi/eCkQ1vqz_8s/0.jpg)](https://www.youtube.com/watch?v=eCkQ1vqz_8s)





