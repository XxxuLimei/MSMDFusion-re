# MSMDFusion-re  
1. 预处理nuscenes：
```
(base) xilm@xilm-MS-7D17:~/fuxian/MSMDFusion-main$ python tools/create_data.py nuscenes --root-path /media/xilm/LENOVO_USB_HDD/data_new/v1.0-trainval01_blobs --out-dir /media/xilm/LENOVO_USB_HDD/data_new/v1.0-trainval01_blobs --extra-tag nuscenes
======
Loading NuScenes tables for version v1.0-trainval...
23 category,
8 attribute,
4 visibility,
64386 instance,
12 sensor,
10200 calibrated_sensor,
2631083 ego_pose,
68 log,
850 scene,
34149 sample,
2631083 sample_data,
1166187 sample_annotation,
4 map,
Done loading in 19.561 seconds.
======
Reverse indexing ...
Done reverse indexing in 3.8 seconds.
======
total scene num: 850
exist scene num: 850
train scene: 700, val scene: 150
[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>] 34149/34149, 30.4 task/s, elapsed: 1124s, ETA:     0s
train sample: 28130, val sample: 6019
======
Loading NuScenes tables for version v1.0-trainval...
Traceback (most recent call last):
  File "/home/xilm/fuxian/MSMDFusion-main/tools/create_data.py", line 219, in <module>
    nuscenes_data_prep(
  File "/home/xilm/fuxian/MSMDFusion-main/tools/create_data.py", line 62, in nuscenes_data_prep
    nuscenes_converter.export_2d_annotation(
  File "/home/xilm/fuxian/MSMDFusion-main/tools/data_converter/nuscenes_converter.py", line 345, in export_2d_annotation
    nusc = NuScenes(version=version, dataroot=root_path, verbose=True)
  File "/home/xilm/anaconda3/lib/python3.9/site-packages/nuscenes/nuscenes.py", line 79, in __init__
    self.sample_data = self.__load_table__('sample_data')
  File "/home/xilm/anaconda3/lib/python3.9/site-packages/nuscenes/nuscenes.py", line 137, in __load_table__
    table = json.load(f)
  File "/home/xilm/anaconda3/lib/python3.9/json/__init__.py", line 293, in load
    return loads(fp.read(),
  File "/home/xilm/anaconda3/lib/python3.9/json/__init__.py", line 346, in loads
    return _default_decoder.decode(s)
  File "/home/xilm/anaconda3/lib/python3.9/json/decoder.py", line 337, in decode
    obj, end = self.raw_decode(s, idx=_w(s, 0).end())
  File "/home/xilm/anaconda3/lib/python3.9/json/decoder.py", line 355, in raw_decode
    raise JSONDecodeError("Expecting value", s, err.value) from None
json.decoder.JSONDecodeError: Expecting value: line 34131442 column 1 (char 1246899200)
```
## 1025:  
1. nuscenes数据集终于就绪！
```
(learnROS) xlm@xlm-Legion-Y7000P-IAH7:~/fuxian/MSMDFusion-main$ python tools/create_data.py nuscenes --root-path /media/xlm/Elements/nuscenes/NUSCENES_TRAINVAL_DATASET_ROOT --out-dir /media/xlm/Elements/nuscenes/NUSCENES_TRAINVAL_DATASET_ROOT --extra-tag nuscenes
/home/xlm/anaconda3/envs/learnROS/lib/python3.9/site-packages/mmdet3d/core/evaluation/kitti_utils/eval.py:10: NumbaDeprecationWarning: The 'nopython' keyword argument was not supplied to the 'numba.jit' decorator. The implicit default value for this argument is currently False, but it will be changed to True in Numba 0.59.0. See https://numba.readthedocs.io/en/stable/reference/deprecation.html#deprecation-of-object-mode-fall-back-behaviour-when-using-jit for details.
  def get_thresholds(scores: np.ndarray, num_gt, num_sample_pts=41):
======
Loading NuScenes tables for version v1.0-trainval...
23 category,
8 attribute,
4 visibility,
64386 instance,
12 sensor,
10200 calibrated_sensor,
2631083 ego_pose,
68 log,
850 scene,
34149 sample,
2631083 sample_data,
1166187 sample_annotation,
4 map,
Done loading in 54.641 seconds.
======
Reverse indexing ...
Done reverse indexing in 3.5 seconds.
======
total scene num: 850
exist scene num: 850
train scene: 700, val scene: 150
[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>] 34149/34149, 34.3 task/s, elapsed: 996s, ETA:     0s
train sample: 28130, val sample: 6019
======
Loading NuScenes tables for version v1.0-trainval...
23 category,
8 attribute,
4 visibility,
64386 instance,
12 sensor,
10200 calibrated_sensor,
2631083 ego_pose,
68 log,
850 scene,
34149 sample,
2631083 sample_data,
1166187 sample_annotation,
4 map,
Done loading in 64.369 seconds.
======
Reverse indexing ...
Done reverse indexing in 3.6 seconds.
======
[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>] 28130/28130, 2.4 task/s, elapsed: 11881s, ETA:     0s
======
Loading NuScenes tables for version v1.0-trainval...
23 category,
8 attribute,
4 visibility,
64386 instance,
12 sensor,
10200 calibrated_sensor,
2631083 ego_pose,
68 log,
850 scene,
34149 sample,
2631083 sample_data,
1166187 sample_annotation,
4 map,
Done loading in 72.826 seconds.
======
Reverse indexing ...
Done reverse indexing in 3.7 seconds.
======
[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>] 6019/6019, 2.2 task/s, elapsed: 2791s, ETA:     0s
Create GT Database of NuScenesDataset
[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>] 28130/28130, 0.9 task/s, elapsed: 29902s, ETA:     0s
load 65262 truck database infos
load 161928 pedestrian database infos
load 339949 car database infos
load 2120 movable_object.debris database infos
load 62964 traffic_cone database infos
load 8846 motorcycle database infos
load 2259 static_object.bicycle_rack database infos
load 19195 movable_object.pushable_pullable database infos
load 11 vehicle.emergency.ambulance database infos
load 11050 construction_vehicle database infos
load 19202 trailer database infos
load 107507 barrier database infos
load 8185 bicycle database infos
load 12286 bus database infos
load 498 vehicle.emergency.police database infos
load 751 human.pedestrian.stroller database infos
load 619 animal database infos
load 492 human.pedestrian.wheelchair database infos
load 352 human.pedestrian.personal_mobility database infos
Traceback (most recent call last):
  File "/home/xlm/fuxian/MSMDFusion-main/tools/create_data.py", line 233, in <module>
    nuscenes_data_prep(
  File "/home/xlm/fuxian/MSMDFusion-main/tools/create_data.py", line 60, in nuscenes_data_prep
    nuscenes_converter.create_nuscenes_infos(
  File "/home/xlm/fuxian/MSMDFusion-main/tools/data_converter/nuscenes_converter.py", line 36, in create_nuscenes_infos
    nusc = NuScenes(version=version, dataroot=root_path, verbose=True)
  File "/home/xlm/anaconda3/envs/learnROS/lib/python3.9/site-packages/nuscenes/nuscenes.py", line 62, in __init__
    assert osp.exists(self.table_root), 'Database version not found: {}'.format(self.table_root)
AssertionError: Database version not found: /media/xlm/Elements/nuscenes/NUSCENES_TRAINVAL_DATASET_ROOT/v1.0-test
```
```
(learnROS) xlm@xlm-Legion-Y7000P-IAH7:~/fuxian/MSMDFusion-main$ python tools/create_data.py nuscenes --root-path /media/xlm/Elements/nuscenes/NUSCENES_TEST_DATASET_ROOT --out-dir /media/xlm/Elements/nuscenes/NUSCENES_TEST_DATASET_ROOT --extra-tag nuscenes
/home/xlm/anaconda3/envs/learnROS/lib/python3.9/site-packages/mmdet3d/core/evaluation/kitti_utils/eval.py:10: NumbaDeprecationWarning: The 'nopython' keyword argument was not supplied to the 'numba.jit' decorator. The implicit default value for this argument is currently False, but it will be changed to True in Numba 0.59.0. See https://numba.readthedocs.io/en/stable/reference/deprecation.html#deprecation-of-object-mode-fall-back-behaviour-when-using-jit for details.
  def get_thresholds(scores: np.ndarray, num_gt, num_sample_pts=41):
======
Loading NuScenes tables for version v1.0-test...
23 category,
8 attribute,
4 visibility,
0 instance,
12 sensor,
1800 calibrated_sensor,
462901 ego_pose,
15 log,
150 scene,
6008 sample,
462901 sample_data,
0 sample_annotation,
4 map,
Done loading in 5.590 seconds.
======
Reverse indexing ...
Done reverse indexing in 0.4 seconds.
======
total scene num: 150
exist scene num: 150
test scene: 150
[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>] 6008/6008, 751.2 task/s, elapsed: 8s, ETA:     0s
test sample: 6008
```
