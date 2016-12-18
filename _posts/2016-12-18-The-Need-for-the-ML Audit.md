---
published: true
---
## The Need for the ML Audit

As the first real post of substance on this site, below is an article about the coming need for machine learning audits that I wrote two months ago for the MIS training institute. I hope you find value from it!

Machine learning algorithms are permeating our world. With 
applications in banking, social media, advertising, and crime 
prevention, to name a few, these ‘little black boxes’ are 
increasingly being used to inform and drive decisions about our 
lives. But how do we know that in high-stakes situations, such as 
prison sentencing, credit authorization, and [soon which person or persons to kill](https://www.technologyreview.com/s/542626/why-self-driving-cars-must-be-programmed-to-kill) are the algorithms really intellectually sound and in our best 
interests? Machine learning models are evaluated and tested by 
their accuracy against a holdout of the model training data know 
as the 'test set'. Machine learning as a discipline attempts to 
predict an outcome and reduce prediction error. A model may be 
theoretically and mathematically functioning correctly but not 
achieving what it aims to accomplish. An excellent example of 
this was given in a paper by Dr. Carlos Guestrin, the Amazon 
Professor of Machine Learning at the University of Washington, 
and his graduate students Sameer Singh and Marco Tulio Ribeiro in 
their paper: [“Why Should I Trust You?” Explaining the Predictions of Any Classifier](http://www.kdd.org/kdd2016/papers/files/rfp0573-ribeiroA.pdf)

Their example was a model that was looking at a picture of a 
dog and predicting whether the dog in the picture was of a husky 
or a wolf. The model did a very good job of predicting whether 
the picture was of a wolf or husky; however, there was one 
problem: all of the wolf pictures on which the model was trained 
had snow in the background. So occasionally when an image of a 
husky with snow in the background appeared, the image would be 
classified as a wolf and vice versa. Now, imagine if this 
algorithm was acting as a gatekeeper to letting dogs into a 
children's park. Well, we won't go there.

Currently, machine learning algorithms in the wild are curated by 
a few well trained “data geeks” who are experts in acquiring 
data, cleaning it, transforming it, and making prediction models. 
However, these individuals are not trained in the intricacies of 
risk analysis and general enterprise governance. Are these newly 
employed algorithms that are increasingly being uses to guide 
decisions producing the desired effect for the organization? An 
objective, third party audit of these algorithms is needed to be 
sure the brain child of the few is serving the needs of the many, 
the organization. Additionally, it most likely won't be long 
before legal precedence and/or regulatory scrutiny come to bear 
on these arcane mathematical models that are increasingly 
affecting enterprise decision making. Who better to provide 
assurance of their accuracy than internal and external auditors? 

Auditing machine learning algorithms is tricky, however, 
requiring extensive knowledge of the data science and machine 
learning fields in addition to industry knowledge and 
organizational risk appetite. How would one go about evaluating 
the efficacy of an algorithm, even if these skills were readily 
available? Dr. Guestrin and his students produced the Local 
Interpretable Model-Agnostic Explanation (“LIME”) framework for 
evaluating classifiers and regressors, two types of machine 
learning algorithms. LIME provides a framework for humans to 
evaluate and understand how an algorithm operates at a local 
level, meaning a number of samples are pulled from the model and 
mini-explanation models are built around the samples. From our 
previous example, the mini-explanation model would explain why 
the sample image was classified a certain wolf as a wolf or husky 
as a wolf. This is brand new research, with the paper being 
released in August 2016 at the KDD conference in San Francisco. 
However, this research provides a starting point for the task of 
making a ML Audit framework.

With machine learning becoming ever more ingrained within leading 
organizations, the need for an independent, objective 
verification of their assumptions and their affect on the 
enterprise's risk tolerance is needed. Internal and external 
auditors are in the perfect position to provide this assurance; 
however the technical competence hurdles are hard to overcome for 
many firms and departments. With the advent of model evaluation 
frameworks, such as Dr. Guestrin and team's LIME project, ML 
assurance can become a reality. 

Andrew
