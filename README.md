# 🔶🤖 AgroVision: Explanation on the model 🔶🤖

Here you'll see the last modification we did on the the notebook, or rather the model that we ended up saved. The dataset we used are gathered and unified from various sources on Kaggle and Mendeley. We choose the top four from the [top ten commodities in Indonesia](https://databoks.katadata.co.id/datapublish/2022/02/10/10-komoditas-pertanian-paling-banyak-diproduksi-di-indonesia) that are reachable to be analyzed (palm oil is not ideal for this type of app). 

We split the roughly 25.000 images on the dataset into 80:20 split for training and validating. We use data augmentation on training set for further decrease overfitting on the model. Then we use MobileNet and customized the end nodes and re-train the whole model with our dataset. This mean we dont use the pre-existing weight that the MobileNet provide and we obtain a satisfying result of 85% accuracy on the validation set.

You may notice that there's another model trained below, we actually tested the model again with 50 epochs just to make sure that the chosen 15 are sufficient for the model before it fluctuates. And sure enough as you'll see on the notebook, it starts to fluctuate greatly at around 20+ epochs.
