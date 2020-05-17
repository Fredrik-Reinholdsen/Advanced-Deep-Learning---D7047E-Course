## Advanced-Deep-Learning---D7047E-Course

# Exercise 1: Setting up and using DeepDIVA
1. Download and prepare the CIFAR10 dataset, command: python util/data/get_a_dataset.py --dataset CIFAR-10 --output-folder toy_datasets

2. Run Image Classification with seed 42, command: python template/RunMe.py --dataset-folder toy_datasets/CIFAR10 --seed42 --ignoregit --no-cuda. Resulting Accuracy: 23.11 %

3. Run previous exercise with Adam optimizer, command: python template/RunMe.py --dataset-folder toy_datasets/CIFAR10 --seed42 --ignoregit --no-cuda --optimizer-name Adam. Resulting Accuracy: 60.45 %

4. Run previous exercise with Adam optimizer, command: python template/RunMe.py --dataset-folder toy_datasets/CIFAR10 --seed42 --ignoregit --no-cuda --optimizer-name Adam --model-name CNN_basic_copy. Resulting Accuracy: 52.94 %

# Exercise 3: t-SNE vs. PCA
In this exercise a basic CNN model has been trained for 10 epochs on the MNIST dataset. Then PCA and t-SNE have been applied to visualize what the network has learned

# Exercise 4: char - RNN
Output “2 b3n”: 
2 b3ne is not that your divising the proceed:
I' the wear be these, I know preceded speed:
It is a sated

Output “bg09Z”: 
bg09ZI will all ungelold durnal;
For he spies for an infire, she dead:
And say me round to whom he look:

Output “qwert”: 
qwert a place and cell, do that?

First Yithart:
Make the sake. My lords of the trumpet of brined,
That t

Output “The”: 
They wherefore men and most ender. Therefore o'
shephembers stopp'd with the strangely senses!

Output “What is”: 
What is these to before us:
The eyes; so that shamelest saw galle the basely.
Here of letter before the blo

Output “Shall I give”: 
Shall I given's rumperation to the sleep.
Simes, where is seo so doth thus to are
are the safety sare of the oth

Output “X087hNYB BHN BYFVuhsdbs”: 
X087hNYB BHN BYFVuhsdbstroy, where you may blow, request,
For my process, for that they pinnall thee.
Like the company, tho

Loss at every 100 epochs: 
1.7783 , 1.5726, 1.4908, 1.4732, 1.3992, 1.4017, 1.4027, 1.3851, 1.3655, 1.3808, 1.3592, 1.3729, 1.3436, 1.3512, 1.3655, 1.3702, 1.3427, 1.3499, 1.3502, 1.3524

# Exercise 5: GANs and adversarial images

Task 1

1.1 
See the "Exercise 5" folder for the modified code used to create the outputs.

1.2
It looks like the generated digits are somewhat more defined, earlier in the training process for the Goodfellow loss. It also seems that the Goodfellow loss one seems
to have a certain affinity for certain digits, particularly 1s and 9s

1.3 
When comparing the the generated images for 20k and 100k training iterations, for both of the loss types we can see a few things. We see that the generated digits become
more defined later in the training process. But we have a wider array of different digits earlier in the training process, particularly for the Goodfellow loss type.
After a while the Goodfellow loss type only produces 1s. This is probably because if the generator produces an especially plausible output it probably learns to produce
only that output. The Goodfellow loss type only produces ones, which might be due to the fact the the digit one, simply being a line, probaly has the least feature variance
and thus is probably easiest to fool the discriminator with, and so the generator learns to produce only ones. 
The results can be improved in a few ways. To take a few examples, one can normalize the input between -1 and +1. One can use different modified loss function.
Or to use a spherical Z instead of using a uniform one.

Task 2

2.1
The adversarial images are carfully constructed to fool out neural network. What the network does is to first to try and construct an input that will result in a selected
label with as high probability as possible. By then looking at what pixels/features maximizes the probabilty of the selected label, noise may be constructed with a similar
character, and then added to any image. This can make the network think that the image is of that particular class, irregardless of its true class.

2.2
Even with random noise as input we are able to get the network to think it is a 9 with 99% certainty, just as in the previous exercise. And the adverserial partial
derivatives seem to have "hotspots" in somwhat the same areas.

2.3 
For the last exercise we used an all zero matrix as input, and we were yet again able to trick the neural network into thinking it´s a 9. This time however with lower certainty, at only 59%. Again the activations appear somewhat similar with "hotspots" and holes in similar places, although it is a bit difficult to tell.
