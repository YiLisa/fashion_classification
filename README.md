# fashion_classification
### Why are you designing the solution in this way?

Firstly, it is a classification problem that asking us to classify the products into 12 categories. We have an image url and a brief description of 1-2 sentences. I choose to use the image to do classification because it is a more intuititive solution. For human, we can tell what is on the image easier than what the text is descripting. In addition, I found it is easier to get training images from the internet. So I choose so start the solution from image classification. I collect 200-400 images per category using google image download tools from github. And then clean and preprocess these data and train the pre-trained VGG16 model for this problem. I choose VGG16 since it has good performance on multiclass classification datasets such as cifar-10. I tried to add 3-4 layers with different hyper parementers, and using 20% of the training data as validation set. The result is based on the best accuacy model. I didn't get a large enough dataset and a powerful GPU to train a new model, so I believe transfer learning is a more efficient appoarch.

### What are the aspects that you considered when designing?

First of all, I considered how I can solve this problem with my knowledge on machine learning with my limited time and computation resource. I am trying to get a satisfactory result on the accurcy of the classification. I also considered the purpose and the possible use cases of the solution. The potential to further improve and add-on to the current solution.

### What are the cases your solution covers, how are they covered and why are they important?
My solution can cover the cases with good image that contains nothing other than the product. I think this is the most important part of this problem. Because this problen is asking me to classify fashion product into 12 given classes, and my solution handled it properly. We can tell most useful information about a fashion product like color, shape, pattern, texture in picture. The product_info.json file only contains information about fashion products, so I am only consider these images in my solution.

### What are the cases your solution does not cover and what are the ways you can extend your current solution for them?
1. My training data didn't include images that is not a fashion product, so if the input is image of other stuff, the classifier would still classify it as a kind of fashion product. For the other category, I used images of other fashion products in the training dataset. If I collect more other random images to get a non-fashion class, that could improve the solution. 
2. I am not combining the description with image to get a comprehensive result. If I can extend my solution to get a result using both image and text as input, it could have a better result.
