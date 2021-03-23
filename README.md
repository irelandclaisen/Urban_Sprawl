# Urban_Sprawl


## Description
In this project, I develop a CNN model to determine if an area is urban or not.  I applied this model to satellite images of Seattle and Las Vegas to measure urban sprawl over time.

## Context
Urban sprawl has a lot of negative impacts, such as air pollution, traffic congestion, destruction of valuable wild life space, and increased carbon emmisions.  Various cities are enacting policies to try to curb urban sprawl and 
it would be interesting to see which cities, and by inference, which policies, are working best to reduce urban sprawl.  One way to measure urban sprawl is to use
satellite images.  It allows for granular and detailed data.  Machine learning can be applied to these satellite images to determine which areas are urban or not urban as a way to measure 
how much an urban area is spreading over times

## Featured Techniques
 * Satellite Image Processing
 * Geospatial Data
 * Convolutional Neural Networks
 * Deep learning
 

## Data
Data was taken from [this link](http://madm.dfki.de/downloads), and satellite images of cities were taken from Google Earth Engine


## Workflow
* Clean satellite image data
* Develop a CNN model to determine if an area is urban or not
* Apply model onto satellite images of Seattle and Las Vegas


## Model
Using the fastai library, I used transfer learning to train a ResNet convolutional neural network to classify satellite images as urban or not urban.  The training data I used was from [this link](http://madm.dfki.de/downloads) which is a land use classification data source.  There are ten categories in which these images are placed: Industrial, Residential, Highway, Annual Crop, Permanent Crop, River Sea/Lake, Vegetation, Pasture and Forest.  Since I was only interested in whether an area could be considered 'urban' or 'non urban,' I divided these 10 categories into two overarching categories, where Industrial, Residental and Highway were considered urban and the other categories were considered non urban.  I also chose to only use the blue, green and red bands of the satellite images.  Upon training a CNN, it was able to get pretty high accuracy and precision on the test data.  


