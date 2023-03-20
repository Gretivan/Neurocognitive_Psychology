 # Documentation 

# October 2022
Thus far, data overview steps and practice exploration has been done. This involved downloading the phenotypic .csv file from the NITRC website and looking at what kind of participants we were working with. More in depth analysis and issues were documented later on as during and before October 2022, the main focus was conceptualising a research question, looking into previous research and attending seminar sessions. 

# November 2022 
# 01.11.2022
This week I reorganised and annotated my githup repository to make it more manageable. I also searched for an atlas that will determine which regions of interest we are assessing. I used research papers assessing cortical thickness differnces in individuals with and without ASD to determine which atlas would be good to use.

# 08.11.2022
This week I assessed the phenotypic information of my data set - including the number of male and female participants, the average age, and the number of autistic vs. control participants. In addition to this I have loaded my atlas in jupyter and loaded the labels for the 148 areas of the Destrieux Atlas. 

# 15.11.2022
Read through course content to get an idea of what the next steps will be, and listed these to get an overview: 
 - establish which brain images to download - aka all the female ppts and some of the male ppts
 - download images, potentially with labels like male-autism, male-control etc. 
 - for preprocessing - merge atlas with the cortical thickness data
 - match the participants - males to females to even out the two groups based on age and group

# 22.11.2022
- use pandas to carry out pattern matching based on a number ot factors aka. age and group 
- plot the new distribution of males and females to see whether they are now more even, and look at the matching accuracy


# 29.11.2022
This week I came across an error while trying to apply and build my mask to my data. After attemtping to google how to apply the mask to my brain images, I decided to get in contact with Peer Herholz. Since I have now matched the participants and know who will be in each group, I can download the necessary files for only those participants which are matched. Phenotypic data can then be reassessed for the new sample. 

# 06.12.2022
After seeking help from Peer we established that my brain images and my atlas were in different spaces which is why they transformations could not be applied. He was able to find a way to resolve this issue using a specific bash code to transform our images into the correct space using ANTs. This took a very long time to figure out, and it did not work with out hiccups which halted my process for a while. 

# 13.12.2022
Since ANTs was not working, I organised the majority of the notebook from what I have done so far, adding commencts of the process along the way. I have again gotten stuck on downloading the whole dataset since there are now new URLs because of the need for transformations. There are files that have no filenames, which I noticed, but this doesnt seem to be a problem now since the new URL requires subject IDs as opposed to file IDs. 

# 20.12.2022
Downloaded all the data, 17 failed downloads so there is a potential need to rematch some of the participants, but this will be decided later. I created a loop to mask all of the data. Before carrying out the loop I rechecked the new sample to assess whether it is too uneven, and whether rematching needs to be done or whether an algorithm can account for this.  

# 07.01.2023
I decided not to rematch the participants but rather use an algorithm that takes this slight mismatch into account. The loop that I created to transform all of the data for future masking didn't work as ANTs failed to execute: the problem being that .bashrc was not being accessed by the syntax, so had to add a path to the ANTs file which took 3 hours. After that, the transformations were completed, creating 311 new transformed files. The files were then masked to create a dictionary of 311 arrays including the 148 areas of the atlas. 

# January, February, March
Due to me starting my Praktikum, I started sporadically working on my Notebook, making small changes here and there without documentation. I started of with the logistic regression analysis which took some time as I came across some problems writing the loop. After this, I decided to add a section before looking into the actual correlations between the different regions of interest, to see whether there were any patterns and relationships between these regions. Next, I was interested in what the results of the logistic regression actually mean, so I plotted two confusion matrices for the two groups and analysed their accuracy using the precision recall f-score and a classification report. The last two things that were of importance to me were a grid search and a feature selection method to see whether this would change anything in my model. 

# 18.03.2023
Some future directions were considered to recommend some aspects that would have been done differently if there had been more time and things that could be added to make a more comprehensive analysis. In addition to this I spent more time finalising and writing for my Jupyter Notebook. 


