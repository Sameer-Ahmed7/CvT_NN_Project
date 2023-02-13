<h1> Convolutions to Vision Transformers <a href="https://colab.research.google.com/github/Sameer-Ahmed7/CvT_NN_Project/blob/main/CVT_Final.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a></h1>


In this nootbook we are going to implement the method proposed in the paper [Introducing Convolutions to Vision Transformers](https://arxiv.org/pdf/2103.15808) (Haiping Wu, in 2021)


>Shahkar Javid - javid.2047305@studenti.uniroma1.it

>Sameer Ahmed - ahmed.2047250@studenti.uniroma1.it





<h2> INTRODUCTION </h2>
<p> In this report we try to re-implement the model proposed in CvT: Introducing Convolutions to Vision Transformers –(Haiping Wu. 2021) [1] for our Neural Network project. This section contains a description of the methods we have implemented, both from the paper perspective and from our point of view. </p>

<h2> General Instruction </h2>

<ul>
<li>We have already pre-trained our model for 350 epoch at bacth size of 512 , saved model can be found in "results" folder of our github repository. <a href = "https://github.com/shahkarKhan24/CvT_NN_Project/tree/main/results/results">[Here]</a>
</li>
<li>Best to download "CVT_Final.ipynb" file on your device rather than colab.</li>
<li>If you wish to run the code and pretrained all over again just run the blocks sequentially.</li>
<li>For pre-training cifar100 dataset must be downloaded.<li>
<li>For fine tuning we have considered catVsdog data set which can be downloaded from <a href = "https://www.microsoft.com/en-us/download/details.aspx?id=54765">[download dataset]</a> [3], and Food dataset with 11 classes which can be downloaded from <a href = "https://www.kaggle.com/datasets/trolukovich/food11-image-dataset?select=training">[download dataset]</a> [5].</li>
<li>Must be connected to a GPU.</li>
<li>Change the Hyper parameter according to your need, it will not give any error but might effect accuracy and training time.</li>
<li>Check and install necessary import library before running the code.</li>
</ul>

<h2> Datasets Details </h2>

| Datasets                   | Classes       | Total images  | Train images  | Test images
| -------------              |:-------------:| -------------:|--------------:|-----------:
| Cifar100 (Pretrained)      | 100           |   60000       |   50000       |  10000
| Cat Vs Dog (Fine-Tuning)   | 2             |   24998       |   17499       |  7499
| Food dataset (Fine-Tuning) | 11            |   13434       |   9404        |  4030

<h2>Install Libraries</h2>
<p>Run below block only if the mentioned library are not already installed.</p>

```python
!pip install einops
!pip install torch
!pip install numpy
!pip intall matplotlib
```
