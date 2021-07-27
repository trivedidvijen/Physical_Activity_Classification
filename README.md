# Physical Activity Classification

## Introduction

This project was developed as part of the online course [PH526x: Using Python for Research](https://courses.edx.org/certificates/1d52e8cf337f4fea98b4ee9b1cb79608) on [edX](https://www.edx.org/course/using-python-for-research?index=product&queryID=6112750093c920d349efe73feaba54b7&position=1) during May 2021. This course was offered by [HarvardX](https://www.edx.org/school/harvardx)

Course Instructor: [Jukka-Pekka "JP" Onnela](https://www.hsph.harvard.edu/onnela-lab/)

## Problem Statement

Physical Activity Classification (e.g. standing, walking, going upstairs or downstairs) from tri-axial smartphone accelerometer data. Smartphone accelerometers are very precise, and different physical activities give rise to different patterns of acceleration.

## Input Data

The input data used for training in this project consists of two files. The first file, [train_time_series.csv](https://courses.edx.org/assets/courseware/v1/b98039c3648763aae4f153a6ed32f38b/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/train_time_series.csv), contains the raw accelerometer data, which has been collected using the [Beiwe research platform](https://github.com/onnela-lab/beiwe-backend), and it has the following format:

timestamp, UTC time, accuracy, x, y, z

The last three columns, here labeled x, y, and z, correspond to measurements of linear acceleration along each of the three orthogonal axes.

The second file, [train_labels.csv](https://courses.edx.org/assets/courseware/v1/d64e74647423e525bbeb13f2884e9cfa/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/train_labels.csv), contains the activity labels, and we'll be using these labels to train our model. Different activities have been numbered with integers. We use the following encoding: 1 = standing, 2 = walking, 3 = stairs down, 4 = stairs up. Because the accelerometers are sampled at high frequency, the labels in [train_labels.csv](https://courses.edx.org/assets/courseware/v1/d64e74647423e525bbeb13f2884e9cfa/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/train_labels.csv) are only provided for every 10th observation in [train_time_series.csv](https://courses.edx.org/assets/courseware/v1/b98039c3648763aae4f153a6ed32f38b/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/train_time_series.csv).

## Activity Classification

We will classify different physical activities. To test the model, we are also provided a file called [test_time_series.csv](https://courses.edx.org/assets/courseware/v1/1ca4f3d4976f07b8c4ecf99cf8f7bdbc/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/test_time_series.csv).

The file called [test_labels.csv](https://courses.edx.org/assets/courseware/v1/72d5933c310cf5eac3fa3f28b26d9c39/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/test_labels.csv) is provided, but it only contains the time stamps needed for prediction; we'll augment this file by adding the corresponding class predictions (1,2,3,4).

## Dataset Files

The four files needed in this project are:

1. [train_labels.csv](https://courses.edx.org/assets/courseware/v1/d64e74647423e525bbeb13f2884e9cfa/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/train_labels.csv)
2. [train_time_series.csv](https://courses.edx.org/assets/courseware/v1/b98039c3648763aae4f153a6ed32f38b/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/train_time_series.csv)
3. [test_labels.csv](https://courses.edx.org/assets/courseware/v1/72d5933c310cf5eac3fa3f28b26d9c39/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/test_labels.csv)
4. [test_time_series.csv](https://courses.edx.org/assets/courseware/v1/1ca4f3d4976f07b8c4ecf99cf8f7bdbc/asset-v1:HarvardX+PH526x+2T2020+type@asset+block/test_time_series.csv)

A fresh copy of these files can also be found under the [dataset csv files](./dataset%20csv%20files/) folder of the repository.

## Methods and Project Report

A project report was developed with all the approach used, methods, final model, train and test accuracy as a Jupyter Notebook. Refer to [final_project.ipynb](./final_project.ipynb).

Additionally for reference course notes are also provided in form of multiple Jupyter Notebooks. It can be found under [course notes](./course%20notes/) folder of the repository.