# Project Description and Approach

The goal of the project is to use BERT (Bidirectional Encoder Representation from Transformers) to predict masked 23s rRNA sequence. First we clean the data to get rid of unwanted characters. Then we mask 15% of the data and see how well BERT does to predict those masked tokens. We use the Jensen Shannon Divergence as our evaluation metric. 

We want to see how the model performs for different tokenization splits : Single, Double and Triple NT sequences. 



# Results 
Note that I only ran a subset of the data due to computational reasons. If I used a small batch size, the training on my current compute would take roughly around 34 days of continous training. I couldn't use a larger batch size for memory reasons. If you have the computational power then you can try running it on the whole subset. For the subset I chose, here are the results I got (Jensen Shannon Divergence is my evaluation metric): 

1 NT: 0.012711929305466389

2 NT: 0.29828839692001763

3 NT: 0.0050884016261092384

Showing that the triple nucleotide performs the best. 


# How to Replicate
Here are some things to keep in mind to replicate the results: 

1) Change the path to where the files are stored in your directory. They're currently set to my google drive so running this notebook alone won't work. 
2) If you have more compute, you'd want to increase the number of training samples. You'd also want to change the batch size.
3) You could also mess around with the learning rate. 
