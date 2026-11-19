员工行为检测数据集，18000张，支持yolo+voc格式
适合做员工行为分析、工厂安全管理、行为识别相关研究用，数据量大，直接可用![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ed47670bfcb84baf8f5305f470763c9e.png)



类型ID 类别名称 图像数量 标注框数量![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6ce10b99c4b447ac888c4e67719252a1.png)

0 fall（摔倒） 8,699 8,751
1 standing（站立） 4,993 8,898
2 sitting（坐） 4,287 5,453
3 front_downsleep（趴睡） 4,226 5,069
4 upsleep（仰睡） 3,432 4,431![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/70f81df8e30d4ed2b4ef19f8ecedbeee.png)

5 back_downsleep（侧睡/背睡） 3,662 4,759

# 员工行为检测数据集
|项目|详情|
| ---- | ---- |
|数据集名称|员工行为检测数据集|
|标注格式|YOLO、VOC|
|样本总量|18000张|
|适用场景|工厂车间员工行为分析、厂区安全管控、离岗/瞌睡摔倒异常行为识别、AI行为识别算法训练|

### 类别明细
|类别ID|类别名称|中文释义|图像数量|标注框数量|
| ---- | ---- | ---- | ---- | ---- |
|0|fall|摔倒|8699|8751|
|1|standing|站立|4993|8898|
|2|sitting|坐|4287|5453|
|3|front_downsleep|趴睡|4226|5069|
|4|upsleep|仰睡|3432|4431|
|5|back_downsleep|侧睡/背睡|3662|4759|

### 应用价值
面向工厂监控场景，识别员工摔倒、在岗瞌睡等危险、违规行为，实现智能化安防与考勤行为监管，适配YOLO系列目标检测模型训练。
```python
# YOLOv11n训练脚本
from ultralytics import YOLO

if __name__ == '__main__':
    model = YOLO("yolov11n.pt")
    model.train(
        data="worker_behavior.yaml",
        epochs=80,
        imgsz=640,
        batch=8,
        device=0
    )
```

