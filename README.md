# tracking_lib
　　The LiDAR tracking library, for tracking objects obtaining from segmentation-based detection and improve segmentation.
<p align="center">
    <img src="figs/demo1.gif" width="720px" alt=""/>
    <img src="figs/demo2.gif" width="720px" alt=""/>
</p>
## How to use
1. We name your ros workspace as `CATKIN_WS` and `git clone` as a ROS package.
    ```bash
    
    # we recommand you to organize your workspace as following
    $ mkdir -p ~/tracking_ws/src
    
    # git clone basic common libraries
    $ cd ~/tracking_ws/src
    $ git clone https://github.com/xiaxin2000/aeng_563_detection_tracking.git
    
    # build your ros workspace for our Tracking-help segmentation demo
    $ cd ~/tracking_ws
    $ catkin_make

    
2. Run demo with kitti rosbag:
    + **Terminal 1**: rosbag play kitti_2011_09_26_drive_0017_synced.bag (https://drive.google.com/file/d/1yJ7xFdPbLgASEE47FuTSNHeCqHDLvpqe/view?usp=sharing)

    + Play rosbag and modify the `detection.yaml` and `tracking.yaml` if necessary.
      
    + **Terminal 2**: launch **Tracking-help Segmentation** demo.
      
        ```bash
        $ cd ~/tracking_ws
        $ source devel/setup.bash
        $ roslaunch tracking_lib demo.launch
        ```

## [Parameters](./launch/demo.launch)
　*detection.yaml* and *tracking.yaml* configure the detection_node and tracking_node in sample. *kitti/\*.yaml* configure the algorithm parameters for KiTTI Dataset, *Segmenter.yaml* and *TrackingWorker.yaml* separately for **Seg-based Segmentation**, **Tracking**.
```bash
./config
├── detection.yaml
├── kitti
│   ├── Segmenter.yaml
│   └── TrackingWorker.yaml
└── tracking.yaml
```

## TODO lists
<p align="center">
    <img src="figs/Tracking-help Segmentation.png" width="480px" alt=""/>
</p>
