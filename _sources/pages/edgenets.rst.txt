================================================================
How to Train for Object Detection Using the EdgeNets Repository
================================================================

This document describes how to use the ``train_detection.py`` script from the EdgeNets repository for training your own object detection dataset. By default, the script is configured to train with the PASCAL VOC datasets (2007 and 2012) and the COCO 2017 dataset. We just need to do two things: i) emulate our dataset to follow the COCO dataset structure, and ii) train the dataset.


Dataset Structure
-----------------

Our dataset should be organized (in the image of COCO) as follows:

  #. Let the name of the root folder be ``BeautifulWater``.
  #. In the root folder, create two folders called ``images`` and ``annotations``.
  #. In the images folder, create two folders called ``train`` and ``val``.
  #. Put the training and validation images in those two folders. Give only numeric names to the images.
  #. Create two JSON files in the annotations folder: ``train.json`` and ``val.json``.
  #. The JSON files should follow the `COCO Data format <http://cocodataset.org/#format-data>`_. We only care about the basic and the Object Detection data structure. Many fields in the data structures are irrelevant to us. We don’t care about the “segmentation” field either.

See `this <http://www.immersivelimit.com/tutorials/create-coco-annotations-from-scratch/>`_ article for details.
