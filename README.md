# Finetune-Segment-Anything-Model-SAM-on-custom-dataset

1. Create a dataset for segmentation.
2. Go to https://app.roboflow.com/ and upload the dataset.
3. Create bounding boxes for segmentation of the interested region on the image. Use
   roboflow's smart annotation to make polygon masks.
4. Use roboflows's augmentation tools if necessary.
5. Export the dataset in YOLO format. This format has the class label at the beginning,
   rest are the coordinates of either the bounding box or the polygon mask.
6. Make a binary mask using Binary_Mask_for_SAM.ipynb file. SAM expects white for the
   interested region (foreground) and black elsewhere (background).
7. Use one of the custom training files for training.
8. Training with box prompt gives better result than training with no prompt. 
