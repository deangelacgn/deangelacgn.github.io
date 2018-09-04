---
layout: post
title:  "How to Build a Search Engine from Scratch - Part 0"
date:   2018-08-13 21:05:13 -0300
categories: tutorials
---

Have you ever wondered how does Google search work? Most of the time, it gives you exactly the results you need based only on a few input words. 

## What is a search engine?
Search engines are basically programs designed to search for items in a database that matches a query given by the user. They can be built to run locally or be web-based applications, and the items searched can be of any type: web pages, images, videos, etc. But the concepts of information retrieval and data mining required to do so are basically the same.
To better understand how it works, how about trying to build our own search engine using Python 3?

## Searching for talks
 In this tutorial series, you are going to learn how to build a search engine for **TED talks**, so that we can find the talks more related to topics(or combination of them) we are interested in. I’ll call it **TEDFinder**, and by the end of this tutorial it should be looking like this:

 ![TEDFinder](https://media.giphy.com/media/1kI8UkK8qMWowQah0r/giphy.gif "TEDFinder")

## Set up
We’re going to develop it in the following environment:

- Python 3.5.0
- Django 2.0.1
- Scikit-Learn 0.18.1
- Numpy 1.13.3
- NLTK 3.2.5

You can download the [list of all packages required](https://github.com/deangelacgn/TEDFinder/blob/master/requirements.txt) in this link and install them by running:

``pip install -r requirements.txt``

## Database
We are going to use a collection of TED talks transcripts as our database. They were provided by Rounak Banik on Kaggle, and can be easily downloaded here in case you don’t have a Kaggle account. It contains all talks uploaded to the official TED website until September 21st, 2017, summing up to a total of 2465 talks.

The database is in CSV format and has only two fields:

- Transcript- The whole transcript of each talk
- URL- The video url corresponding to the talk transcript
