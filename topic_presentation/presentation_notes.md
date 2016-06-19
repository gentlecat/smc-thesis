## Slide 1 - Title

Hello!

My project is going to be related to datasets that are used within the MIR community. 

## Slide 2 - Motivation

Datasets are one of the most important parts of different research tasks, and unfortunately their quality is a bit of a problem. Datasets and machine learning algorighms generated from them don't produce good enough results.

So last year AcousticBrainz project was started and these problems became obvious after users started to analyse their music collections, which are much more extensive compared to what is available within the MIR community. And we already have more than 3 million submissions.

And so the problem with currently used datasets is that most of them contain no more than a 1,000 recordings, structure of these datasets is not good enough either. For example datasets for genre classification contain no more than 10 genre labels in them.

Another big problem is that some of these datasets are not publically available, so it's impossible to iterate on them, make improvements, try to get better results.

## Slide 3 - Goals

So the goal of the project is to find a way, find what kind of tools people need to create datasets of better quality. The plan is to create an open framework with different tools for creation and try to understand what will help us to improve the actual quality of the output, which can be accuracry of classification from models produced using these datasets, or whatever other metric that we choose.

In terms of tools, we already have a basic version of dataset creation and evaluation tool. It allows people to create their own collections of recodings and generate models for extracting high-level information from music like genre, mood, what have you...

And all that is kind of a foundation for different tools. It's still an open question on what's needed to improve quality of datasets.

## Slide 4 - Methodology

There are several different things we plan to try.

Aguarbly, the most important one is to streamline the interface for working with datasets. The only two ways to create them in our current system is by importing CSV file with a list of classes and reordings in them, or manually by addinng MusicBrainz IDs of recordings one by one.

So first we need to simplify process of manual creation, which can be very tedious right now, especially if you work with large datasets. We have to allow people to search for recordings without requirering them to deal with UUIDs, maybe even allow to add whole albums. Then there needs to be an API, which would allow developers to build on top of what we have and create additional tools for themselves.

It would also be great to allow people to collaborate on creation. Collaboration can be in a form of actually allowing to edit one dataset at the same time, kind of like Google Docs. And we can try something like fork/merge model from Git.

We can try to create lists of recordings that correspond to a particular class. And then dataset creators can take a look at all the lists that we provide and incorporate them within their datasets. These lists can be created using tags or labels that people put on recordings.

Another important part of creation process is actually improving results that you get. But to make meaningful improvements there needs to be a feedback loop. So what we can do is allow people to extract high-level information from recordings that people submit using a model. And then we allow other people to provide feedback on results that they get. Then creator can see what are the issues and make adjustments to the dataset.

The last big idea is to encourage people to improve datasets by organizing "dataset challenges" within MIR and AcousticBrainz communities. ...

We'll be able to evaluate usefulness of the framework by measuring accuracy improvements that datasets created within it will produce, compared to other datasets that already exist within the community.
