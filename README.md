# liver_tumor

## log
* 2018/05/10 check the dataset
* 2018/05/13 split nifti into pictures
* 2018/05/14 try the UNet
  * scale down pictures to train faster and to allow bigger batch size

## next steps
* in terms of IOU, the model predicts badly for smaller targets
* train_loss:0.0031; val_loss: 0.0038; test_loss: 0.03
  * the difference between val_loss and test_loss is large
  * val set and test set should be sampled from same distribution
  * val set and test set probably have different target size distribution
  * inspect the relation between loss and target size
  * resample val set to make val set similiar to test set
  * data augamentation, regularization might help
* H-DenseUNet and DenseUNet looks cool
