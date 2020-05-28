# Interview Emanuel Oehri, 27.05.2020
To evaluate the performance of the embedding space trained on the music dataset, mister Emanuel Oehri will be interviewed. This document represents the interview guide.

## Describe project and status
The goal of the project is to create an embedding space for noise detection and music dataset by adapting triplet loss to an unsupervised setting. Therefore no label is used to train the model and will be only used to evaluate the model performance. 

The embedding space should be able to represent meaning, and the distances of embedded samples should represent the similarity between them. 

Both of the embedding space models use the same hyperparameters, except for the segment size, neighbouring range and sample rate. The difference in hyperparameters in mainly because the music dataset has the possibility of using larger segments and therefore also a wider neighbouring range since each song is available as full audio.

The experiments for the DCASE dataset (noise detection) are finished, and the embedding space was examined. To compare the performance with the results from the challenge, a simple logistic classifier was trained using the embedding space as an input. The best performing embedding architecture accomplished a macro-averaged F1 score of 62.9%, which is a 20% gap between the model of the thesis and the submitted results of the challenge. However, when examining the embedding space, a few interesting properties were found. The embedding space can:

- find misclassified sound segments in the dataset, by merely looking at the neighbourhood of each sample
- find microphone malfunctions in the dataset, by merely looking at the neighbourhood of each sample
- represent the underlying sound it represents and builds clusters, for example in the embedding space a "silence cluster" was observed
- generate audio files which "walk through the embedding space" from one label to the other

The experiments using the music dataset, provided by mister Emanuel Oehri, are now also finished and the embedding space was examined. While examining the embedding space, a few exciting properties were found and will be discussed in this interview.

## Ressources
> All of the sound segments are 10s long, and the neighbouring range is 40s wide. As a neighbourhood in the embedding space, the closest three are considered.

- (R1) Soundcloud playlist: song created by appending sound of segments together, where the neighbourhood is not consistent
- (R2) Soundcloud playlist: song created by appending sound of segments together, to represent a walk through the embedding space from label to label
- (R3) Image of K-Means clustering visualised by using two principal components

## Interview
1. Did you already have the chance to look at the resources provided before the interview?

2. How similar would you rate the six different categories in the music dataset, from 1 to 10, where ten is very similar?

3. Would you consider the categories as genres or as subgenres of a genre? If subgenre, what would you consider to be the genre?

4. The playlist "cluster centres" are songs which consist of the neighbours of the cluster centre of each label. 

4.a. Does every cluster represent a typical song within the category?

4.b. Did you something strike your attention, where a song stood out for a reason?

5. Categories "Electronica_Downtempo" and "MelodicHouseAndTechno" are not well seperated and songs often have neighbours of both categories.

5.a. How similar would you rate the categories "Electronica_Downtempo" and "MelodicHouseAndTechno", from 1 to 10, where ten is very similar?

5.b. Can you describe the similarity or dissimilarity?

6. The provided audio sample "Neighbours_Electronica_Downtempo_and_MelodicHouseAndTechno.wav" shows the neighbourhood from a segment of the class "Electronica_Downtempo", where the neighbourhood is not consistent. Nevertheless, do you think the audio still sounds similar? (Scale 1 to 10)

7. The similarity between genres, by applying K-Means clustering to the embedding space with 7 clusters.

7.a. Would you consider the genre combinations as reasonable?

7.b. Where do you think the embedding space still has some flaws?

8. Walkthrough space

8.a. Did you find something which did not sound very good?

8.b. Did you find something which sounded very good?

9. Overall, was there something that struck your attention, when listening to the songs?

9.a. In a good way?

9.b. In a bad way?

10. How would you describe the results of the embedding space?

11. Would you consider the experiment to be successful or not?

12. Would you pursue this idea further?





