

What's amenity detection?

Object detection but for common and useful household items someone looking for an Airbnb rental might want to know about. For example, does this home have a fireplace?

Original inspiration was drawn from the article Amenity Detection and Beyond — New Frontiers of Computer Vision at Airbnb.

What's in this repo?
Notebooks with 00-10 are all the steps I took to train the full model, largely unchanged from when I originally wrote them.
For a cleaned up version, see the example Colab Notebook.
preprocessing.py contains the preprocessing functions for turning Open Images images & labels into Detectron2 style.
downloadOI.py is a slightly modified downloader script from LearnOpenCV which downloads only certain classes of images from Open Images, example:
sql
Copy code
# Download only images from the Kitchen & dining room table class from Open Images validation set
!python3 downloadOI.py --dataset "validation" --classes "Kitchen & dining room table"
app contains a Python script with a Streamlit app built around the model, if you can see the live version, Streamlit is what I used to build it.
custom_images contains a series of different images related to the project, including various rooms around my house to test the model.
See how it was done
Daily progress, notes and code in a journal format (since this was a 42-day project, I took notes every day on what I was working on).
YouTube video series starting from the project overview to building a model to deploying a model to wrapping up the project.
All modelling experiments I tracked using Weights & Biases.