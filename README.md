# Crowd-counting-EE626-course-project

This is an implementation of the paper [CSRnet](https://arxiv.org/abs/1802.10062) for crowd counting.\
I have used Google colab to run all phython notebooks.

## Dataset

[ShangaiTech Dataset](https://drive.google.com/drive/folders/1bKs3w-KfFgyweDwVGpAR_QzCEuz6jm2q?usp=sharing)\
I have already created and saved the ground truths using gaussian filters from the linked [repo](https://github.com/davideverona/deep-crowd-counting_crowdnet\n).

## Ground Truth generation 
Use the `CSRnet_create_dataset.ipynb` to generate the ground truth's.\
Note - We have already saved the ground truth in this final datasets.\
If you are planning to run it make sure that the `root` variable is changed to the proper address. 

## Training
Use the `CSRnet_train.ipynb` to train the model and save checkpoints. We have made a 90-10 split to choose the best trained parameters.\
Note that you have to make the splits separately for Part A and B datasets so make sure to change the `task` variable to properly save the checkpoints(state of the model).\
Also change the `root` variable to the address of your folder.

## Testing
Use the `CSRnet_test.ipynb` to test the model using the saved model states.\
Note - Change the `root` variable to the address of your folder.

## Results

|       Dataset       | MAE           |  
| ------------------- | ------------- |
|ShanghaiTech part A  | 88.232        | 
|ShanghaiTech part B  | 16.684        |


## References

1. [CSRnet](https://arxiv.org/abs/1802.10062) for crowd counting.
2. [Crowdnet](https://github.com/davideverona/deep-crowd-counting_crowdnet\n)
