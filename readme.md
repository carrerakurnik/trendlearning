# 

We followed [the official installing tensorflow guide](https://www.tensorflow.org/install/install_mac) with the Virtualenv instructions, and the [image retraining tutorial](https://www.tensorflow.org/tutorials/image_retraining) to get started

We are using Virtualenv with Python 2.7

## Instructions

### Prepare your images

Create a new folder for each category you want to identify and place it into the "training_images" folder. Move any you don't want to use into the "unused_training_images" folder for storage.

### Getting Ready

Open up Terminal and cd into the directory, in our case that looks like: 

1. "cd /Users/carrerakurnik/tensorflow"

Activate the virtual environment by typing

2. "source ./bin/activate"

which should result in the prompt changing to be prepended by (tensorflow)

### Retraining

Next you have to run the retrain.py script inside of this (tensorflow) Virtual env and point to the director that has your training photos, in our case:

3. "python examples/image_retraining/retrain.py --image_dir ~/Desktop/runway_ss_18/training_images"

Run that and it will train the neural net for 20 minutes or more depending on your data set

Place a test image inside of the testing folder and take note of the name and extension.

Run the following command in that same terminal window, change the image name as necessary.

```
python examples/label_image/label_image.py \
--graph=/tmp/output_graph.pb --labels=/tmp/output_labels.txt \
--input_layer=Mul \
--output_layer=final_result \
--input_mean=128 --input_std=128 \
--image=testing/test.jpg
```