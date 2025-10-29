                                                                              # python_study
                                                                              记录代码中不熟悉的语法结构
一.DATASTE处理
  1.def __init__(self, infpre_path, in1k_path, coco_path, transforms=None, spec_dataset=None, use_in1k=False, per_cls_num=200, use_coco=False, data_ratio=1.0, rgb_gray=False):
  #spec_dataset指是否有特色数据集当做训练数据集。per_cls_num每个类别最多使用200个样本。transforms是否进行可传入自定义的数据增强/预处理操作。rgb_gray：是否把图片灰度化。
  2.datasets = os.listdir(infpre_path)。os.listdir用来列出infpre_path文件下面所以文件夹。os.path.join(infpre_path, dataset)用来把两个路径infpre_path和dataset拼接。如下：
    infpre_path/
    dataset1_name/     ← 会被 os.listdir() 获取到
        thermal/
            image1.jpg
            image2.jpg
        rgb/
            image1.jpg
    dataset2_name/     ← 会被 os.listdir() 获取到  
        thermal/
            image1.jpg
        rgb/
            image1.jpg
    dataset3_name/     ← 会被 os.listdir() 获取到
        thermal/
            image1.jpg
        rgb/
            image1.jpg
