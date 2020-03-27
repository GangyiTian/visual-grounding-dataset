Visual grounding数据集制作
=
## ReferCOCO数据集
>1.下载COCO数据集，[官方网站](http://cocodataset.org/#overview) 2014年。<br>
>2.下载ReferCOCO数据集json文件和.p文件。<br>
>  * refcoco:http://bvisionweb1.cs.unc.edu/licheng/referit/data/refcoco.zip
>  * refcoco+:http://bvisionweb1.cs.unc.edu/licheng/referit/data/refcoco+.zip
>  * refcocog:http://bvisionweb1.cs.unc.edu/licheng/referit/data/refcocog.zip <br>

>3.文件结构如下所示:
```
data
|-- refcoco
    |-- instances.json
    |-- refs(google).p
    |-- refs(unc).p
|-- refcoco+
    |-- instances.json
    |-- refs(unc).p
|-- refcocog
    |-- instances.json
    |-- refs(google).p
    |-- refs(umd).p
|-- images
    |-- train2014
  ```
 >4.进入项目文件夹，执行以下命令处理数据集：
 ```
 python data_process.py --data_root data --output_dir data --dataset refcoco --split unc --generate_mask
 python data_process.py --data_root data --output_dir data --dataset refcoco+ --split unc --generate_mask
 python data_process.py --data_root data --output_dir data --dataset refcocog --split umd --generate_mask
 ```
 >处理完成生成anns、masks文件夹，详细细节可访问作者:https://github.com/lichengunc/refer <br>
