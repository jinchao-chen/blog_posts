---
toc: false
layout: post
hide: true
description: weekly post on project development, reading notes, and new skills
categories: [markdown, weekly post]
title: Weekly Post - 01
---
This is the first of my weekly posts. I started weekly posts to track my project progress, share reading notes, and ideas I found inspiring.  

Recently I started the mooc course by [fast.ai](https://course.fast.ai) on Practical Deep Learning for Coders . This week's post is mainly on deeep learning jargons and a hobby project that classifies bear type based on the uploaded image.

## Projects
[bear classifier](https://a-bear-classifier.herokuapp.com): a simple NN that classifies the bear as teddy, black bear or frizzy bear. The model was created using fastai. The training data, labeled images of black, teddy and frizzy bear, was downloaded through Bing image search. The deep learning model deployed using voila on mybinder. 

## Jargons 
**end-to-end iteration**: start iterate from end to end; that is, don't spend months fine-tuning your model, or polishing the perfect GUI, or labelling the perfect dataset. Instead, complete every step as well as you can in a reasonable amount of time, all the way to the end. 

**drivetrain approach** start by defining a clear objective, collect data to support the ultimate objectives, then build a model that you can use to determine the best actions to take to get the best results *in terms of your objective*. [advices on drive train approach for digital products development](https://www.oreilly.com/radar/drivetrain-approach-data-products/)

**Data augmentation** creating random variations of input data. the model can therefore learn from rotated, trimmed or scaled images: data set is augmented by varying the available input data

## Python

A very intuitive example on classmethod and static method

```Python
# how to use a calssmethod 
class Pizza:
    def __init__(self, ingredients):
        self.ingredients = ingredients

    def __repr__(self):
        return f'Pizza({self.ingredients!r})'

    @classmethod
    def margherita(cls):
        return cls(['mozzarella', 'tomatoes'])

    @classmethod
    def prosciutto(cls):
        return cls(['mozzarella', 'tomatoes', 'ham'])

Pizza.margherita()
```

```Python

import math

# static method example 
class Pizza:
    def __init__(self, radius, ingredients):
        self.radius = radius
        self.ingredients = ingredients

    def __repr__(self):
        return (f'Pizza({self.radius!r}, '
                f'{self.ingredients!r})')

    def area(self):
        return self.circle_area(self.radius)

    @staticmethod
    def circle_area(r):
        return r ** 2 * math.pi
```
