# TML_Team9_Model_Stealing

The jupyter notebook provides the code for Model Stealing. Firstly, we have queried the api with all 13k images in intervals of 65 seconds and each query had 1k images. Then, they are stored in the pickle file. 

All the images are converted into Tensors, and Dataset and Dataloader objects are prepared

StolenModel class is used to create a CNN with 3 convolutional layers. The loss function used here is MSE as it produces a loss based on the L2 difference between the output representations and victim representations. L2 loss is 29.9

I also tried augmentations using "StolenEncoder: Stealing Pre-trained Encoders in Self-supervised Learning" paper by Liu et. al. I implemented SimCLR and MaskedAutoEncoders along with contrastive loss (for SimCLR) and soft nearest neighbors loss respectively. However, I couldn't produce good results with them. 
