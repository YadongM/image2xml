# ImageBox2Xml
# 环境
- 配置python 2.7、pip 及opencv3.0 环境

- 需要numpy

- 创建如下目录结构
```
----某一目录（以D:/example/为例，下同）
        |
        -----Annotations #用于保存Xml
          |
          ---JPEGImages #图片
          |
          ---Labels #中间文件 txt文本、
          |
          ---createXml.py
          |
          ---label.py
```

- 将图片文件放入JPEGImages中

# 生成Labels下的txt文件

- 命令行进入文件夹，输入 python label.py


- 点击Load

 
- 点击plate按钮，设置当前类别为plate ，此步骤一定要在绘制框之前进行。（如果有其他类别可在label.py进行拓展）

- 在图片上绘制框（点击两次，不是拖拽），绘制完成后右方列表新增坐标。选定坐标按下Delete按钮可删除该坐标。按下ClearAll可清除全部坐标。

- 绘制完成后按下save按钮，保存当前坐标。

- 点击prev 或者 next按钮进行其他图片的处理（点击同时也有保存效果）

- 可输入指定编号进行跳转

# 生成VOC格式的Xml文件
- 命令行进入文件夹，输入 python createXml.py
