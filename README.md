# Notes on the provided solution
I trained an lenet5 model and added the "idontknow" class based on the curation results.
Because there were so few samples labeled "idontknow", compared to the other samples, I decided to augment them. 
This let to model that did not classify any sample as "idontknow". Sadly I was unable to fix the model.

One reason I could imagine that led to this behaviour is that I did not differentiate between hard samples and mislabeled samples. 
In retrospective it would have been smart to remove the mislabeled (or relabel them) and only train the new model on hard samples.

The cleaned dataset can be found on [hugging face hub](https://huggingface.co/datasets/Linus-L/mnist-cleaned-full)
