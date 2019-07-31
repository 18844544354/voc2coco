# pascol voc to coco
Convert pascol voc annotation xml to COCO json format.

1. pip install lxml
2. python voc2coco.py xmllist.txt ../Annotations output.json

The xmllist.txt is the list of xml file names to convert.
000005.xml
000007.xml
000009.xml

The "../Annotations" is the place where all xmls located.

The "output.json" is the output json file.

以下生成txt文件，包含文件名
import os
path=r'D:\myCode\CornerNet\CornerNet-master\data_bike\bike\Annotations'
files= os.listdir(path)
fp = open('./img_name.txt','w+')
Img_list = os.listdir(path)
for Name in Img_list:
    # fp.write(str) 
    fp.write(Name + '\n ')#会导致末尾有一个空行
fp.close()

#调用
if __name__ == '__main__':
    path = r'D:\myCode\CornerNet\CornerNet-master\data_bike\bike\Annotations'
    convert('img_name.txt', path, 'output.json')
    
