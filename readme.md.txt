# 

We followed [the official installing tensorflow guide](https://www.tensorflow.org/install/install_mac) with the Virtualenv instructions, and the [image retraining tutorial](https://www.tensorflow.org/tutorials/image_retraining) to get started

We are using Virtualenv with Python 2.7

## Instructions

### Getting Ready

Open up Terminal and cd into the directory, in our case that looks like: 

1. "cd /Users/carrerakurnik/tensorflow"

Activate the virtual environment by typing

2. "source ./bin/activate"

which should result in the prompt changing to be prepended by (tensorflow)

### Retraining

Next you have to run the retrain.py script inside of this (tensorflow) Virtual env and point to the director that has your training photos, in our case:

3. "python examples/image_retraining/retrain.py --image_dir ~/Desktop/runway_ss_18/"

Run that and it will train the neural net for 30 minutes or more depending on your data set