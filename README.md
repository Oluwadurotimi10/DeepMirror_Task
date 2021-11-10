# DeepMirror_Task
### Step 1: After researching, I decided to use detectron2 Mask-RCNN implementation for this task because of its easy setup, understandable codebase and active community. The next thing is to fork its [repo](https://github.com/facebookresearch/detectron2) then clone it into your local system.
### Step2: Upload your detectron2 folder to your google drive, since colab will be used for running the notebooks.
### Step 3: Create a [notebook](https://github.com/Oluwadurotimi10/DeepMirror_Task/blob/main/COCO%20datasubset.ipynb) in your working directory for obtaining your desired subset of the COCO dataset. For this task, the Bus category was used. Before running this notebook, download your desired annotations file from the [COCO website](https://cocodataset.org/#download) and upload to your drive. The 2017 train/val annotations was used for this task, and it can be found [here](https://drive.google.com/drive/folders/172xNgg1rkiuJCuqmrdjHYxex9hn7kT1m?usp=sharing)
### Step 4: After preparing the datset, we move into the [instance segmentation notebook](https://github.com/Oluwadurotimi10/DeepMirror_Task/blob/main/InstanceSegmentation.ipynb). Here, the Mask-RCNN model in detectron2 is trained with and without feature noise and inferences were performed. The process is well detailed inside the notebook.
### Step 5: Inorder to add the feature noise to the latent space of the backbone encoder network, you need to find where the specified latent space is located. For this task, I found it in the rcnn.py located [here](https://github.com/Oluwadurotimi10/detectron2/tree/main/detectron2/modeling/meta_arch). The file I made changes (lines 158 to 162) to is located [here](https://drive.google.com/file/d/12tgwF2RgnnZe7zBWzkWBnXd_GrvwLDe_/view?usp=sharing) in my drive.
#### Below is the plot of the training loss without feature noise.
![Without feature noise](https://github.com/Oluwadurotimi10/DeepMirror_Task/blob/main/loss_without_noise.PNG)

#### Below is the plot of the training loss with feature noise.
![With feature noise](https://github.com/Oluwadurotimi10/DeepMirror_Task/blob/main/loss_with_noise.PNG)
