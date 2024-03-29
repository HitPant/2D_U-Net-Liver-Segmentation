# Liver Segmentation - 2D U-Net

![alt-text](https://github.com/HitPant/2D_U-Net-Liver-Segmentation/blob/main/img/seg.png)

![alt-text](https://github.com/HitPant/2D_U-Net-Liver-Segmentation/blob/main/img/unet.png)


### Steps performed:

1. Preparing Dataset:
   Convert dicom files into nifties
   NIfTI is a more widely supported format than DICOM, allowing the data to be opened and analyzed.

2. Batching images silces
   Creating groups of slices(each layer of the volumetric image data)
   Perfomed transformations: Scale intensity, Crop Foreground, orientation, etc.

  ![alt-text](https://github.com/HitPant/2D_U-Net-Liver-Segmentation/blob/main/img/trans.png)

3. Train U-Net model:
   A U-Net model is traine with Pytorch framework.

   ![alt-text](https://github.com/HitPant/2D_U-Net-Liver-Segmentation/blob/main/img/model.png)

   Dice loss is calculated
   Dice Loss = 1 - 2 * (Sum of (Predicted * Ground Truth)) / (Sum of Predicted + Sum of Ground Truth)
   
   ![Image description](https://github.com/HitPant/2D_U-Net-Liver-Segmentation/blob/main/img/dice_loss.png)

