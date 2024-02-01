## Simple CycleGAN realization with Pytorch
### [Kaggle notebook](https://www.kaggle.com/code/kb7354/cyclegan/notebook) | [Saved checkpoints](https://disk.yandex.ru/d/L-_m9OoUCs2ZxA)

This is implementation of CycleGAN  using Pytorch, mostly following the originally proposed architecture
([see here](https://junyanz.github.io/CycleGAN/)). It was trained using datasets of monet and vangogh
painting from the original paper (`cyclegan_testing.ipynb` contains download scripts).

### Some details on training

I trained the models using kaggle's P100 GPU. Initially i set learning rate to $2e-5$ as recommended by the paper.
I used this lr for first 35 epochs, then tried reducing it to $2e-6$. Unfortunately due to limited GPU time I did not
do a lot of experiments, but I noticed that after 45 epochs with rate of $2e-5$ model seems to start overfitting. 