# Documentation


## October 2022
Between the beginning of the Summer and the start of the second semester, the main focus of this project was conceptualizing a research question, looking into previous research and attending seminar sessions. During this time I also looked for a suitable open dataset to use that related to Autism. The only option I found was the ABDIE I dataset which, despite it being open, was very difficult to get access to as the links provided for download on the website were wrong. Peer Herholz helped me get the true link for this dataset so that it could be downloaded without problem. Thus far in terms of analysis, I have started data overview steps and practice exploration. This involved downloading the phenotypic .csv file from the NITRC website and looking at what kind of participants we were working with. I also did a practice download and visualisation of one of the pieces of data to get an idea of what I needed to do in terms of preprocessing. 


## November 2022
### 01.11.2022
This week, I reorganized and annotated my GitBub repository to make it more manageable based on the template repository provided to us. Since I now also have an idea of what data I am working with and that I would need to mask it to make it more manageable and assessable, I also searched for an atlas that will determine which regions of interest we are assessing. I used research papers assessing cortical thickness differences in individuals with and without ASD to determine which atlas would be good to use.

### 08.11.2022
This week I assessed the phenotypic information of my data set - including the number of male and female participants, the average age, and the number of autistic vs. control participants. While looking at this phenotypic information, I noticed that the sex split is very uneven, that being around 70% of the participants were male, so I need to consider what to do about this. In addition to this, I have loaded my atlas in Jupyter and loaded the labels for the 148 areas of the Destrieux Atlas.

### 15.11.2022
Read through course content to get an idea of what the next steps will be. Since the ABIDE I dataset consists of over 1000 large brain images, I was worried about downloading them all at once incase I didnt have the storage space. So I decided to use a matching technique to match the participants the male participants with the female participants, to even out the groups and to establish whether all of the brain images need to be downloaded or only a select amount. For the preprocessing of the data, I have now downloaded and visualised the atlas and built the masker to apply it to the coritcal thickness data. 

### 22.11.2022
This week I carried out pattern matching, to match my female and male participants, based on age and group as a factors. This means that I should now have even sex and ASD/control group sizes. I also plotted the new distribution of males and females to see whether they are now more even, and look at the matching accuracy. 

### 29.11.2022
This week, I came across a major error while trying to apply and build my mask to my data. After attempting to google how to apply the mask to my brain images, I decided to get in contact with Peer Herholz, since I followed the given instructions for applying the masker. In addition to this, I downloaded the necessary files for the participants who were matched and reassessed the phenotypic data for the new sample. 


## Dezember
### 06.12.2022
After seeking help from Peer we established that my brain images and my atlas were in different spaces which is why they transformations could not be applied. He was able to find a way to resolve this issue using a specific bash code to transform our images into the correct space using ANTs. This took a very long time to figure out, and it did not work without hiccups, which halted my process for a while. While in theory his code that he provided me should have worked, I was having a lot of issues with ANTS. 


### 13.12.2022
I finally got ANTs to work for my practice brain image and was able to apply all the transformations as well as the masker which was working too. I organized the majority of the notebook from what I have done so far, adding comments of the process along the way. I have again gotten stuck on downloading the whole dataset, since there are now new URLs because of the need for transformations. There are files that have no filenames, which I noticed, but this doesn't seem to be a problem now since the new URL requires subject IDs as opposed to file IDs.


### 20.12.2022
Since I thought ANTs was finally working, I Downloaded all the data that I needed too, finding that 17 downloads failed. There was potential to rematch some of the participants, but this will be decided later. I created a loop to transform and mask all the data that I had now downloaded. Before carrying out the loop, I rechecked the new sample to assess whether it is too uneven, and whether rematching needs to be done or whether an algorithm can account for this. 

## Janauar
### 07.01.2023
I decided not to rematch the participants, but rather use an algorithm that takes this slight mismatch into account. The loop that I created to transform all the data for future masking didn't work as ANTs failed to execute: the problem being that .bashrc was not being accessed by the syntax, so had to add a path to the ANTs file, which took 3 hours. After that, the transformations were completed, creating 311 new transformed files. The files were then masked to create a dictionary of 311 arrays, including the 148 areas of the atlas.


## January, February
Due to me starting my Praktikum, I started sporadically working on my Notebook, making small changes here and there without documentation. I started off with the logistic regression analysis, which took some time as I came across some problems writing the loop. After this, I decided to add a section before the logistic regression looking into the actual correlations between the different regions of interest, to see whether there were any patterns and relationships between these regions. Next, I was interested in what the results of the logistic regression actually mean, so I plotted two confusion matrices for the two groups and analyzed their accuracy using the precision recall f-score and a classification report. The last two things that were of importance to me were a grid search and a feature selection method to see whether this would change anything in my model.

## March
### 17.03.2023
Today I created the jupyter book and made all the necessary changes to the template to make it look like mine. This included changing the index file, writing a little description and adding a logo. I also tweaked my logistic regression, and added a Selectred K-fold analysis to check whether K-fold feature selection made a difference to my logistic regression scores. 

### 18.03.2023
Some future directions were considered to recommend some aspects that would have been done differently if there had been more time and things that could be added to make a more comprehensive analysis. In addition to this, I spent more time finalizing and writing for my Jupyter Book. 

### 21.03.2023
Today I finished writing the discussion, and tweaking and rereading previous sections made. I came across an issue in my vscode - that being that there was an issue with the formating of the markdown cell in my _toc file, meaning I wasn't able to include sections in my left margins. Michael Ernst helped me resolve this issue. 

### 22.03.2023
The finalisation of the project was done today. This included double checking the text and to see whether all the analsyis aspects were clearly presented. 
