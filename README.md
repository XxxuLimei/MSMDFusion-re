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
