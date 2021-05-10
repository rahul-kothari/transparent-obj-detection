# transparent-obj-detection
COMP 592- Transparent Object Detection - Dissertation

Transfer learning on VGG-19 and Mask R-CNN.

## Set-Up
* upload the [VGG-19.ipynb](VGG-19.ipynb) and [Mask_RCNN.ipynb](Mask_RCNN.ipynb) to Google Colab. This means that you won't have to do any dependency installation at all.
* Mount the google colab ipynb files to your google drive
* Create a folder in google drive where you will host the data, pre-trained models, logs of trained models etc.
* For Mask R-CNN, for easy installation, just upload the 4 files in [mrcnn_updated_code](mrcnn_updated_code) to your folder in google drive
* Upload the data, logs folder there too.

Your google drive directory should now look like:
```bash
├──  data
│   ├── train
│   │   ├── Glass(24).jpg
│   │   ├── ...
│   │   └── region_data_train.json
│   └── val
│       ├── Glass(41).jpg
│       ├──  ...
│       └── region_data_val.json
├── logs
│   ├── mask
│   │   ├── transparentobj20210407T1018
│   │   │   ├── mask_rcnn_transparentobj_0001.h5
│   │   │   ├── mask_rcnn_transparentobj_0002.h5
│   │   │   ├── ...
│   │   └── └── mask_rcnn_transparentobj_0040.h5
│   └── vgg	
│   	└── detector20210414T1433.h5
├── mask_rcnn_coco.h5
├── VGG19.ipynb
├── Mask-RCNN.ipynb
├── config.py
├── model.py
├── utils.py
└── visualize.py
```

* `data` has `train`, `val` folders each with images and 1 annotation file ([`region_data_train.json`](data/train/region_data_train.json) and [`region_data_val.json`](data/val/region_data_val.json) respectively)
* `logs` has the models I trained (mask rcnn and vgg). Mask model was trained on 40 epochs and the model at the end of each epoch is there! Note that because the models were so big (~10 GB), they couldn't be uploaded here. Instead a drive link has been provided. Only 1 epoch has been uploaded here.
* `mask_rcnn_coco.h5` is the original pre-trained mask r-cnn (trained on COCO dataset). This doesn't need to be there if you simply want to try my trained model
* The two .ipynb files are the code I used to output results discussed in my dissertation. Instructions have been provided in each of these files on how to run them.
