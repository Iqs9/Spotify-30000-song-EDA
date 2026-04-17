# Spotify-30000-song-EDA
Using association rule mining can we find a song feature that makes a track popular?
To see if this is true we will use association rule mining (finding if-then relationships).

Results: 

Figure 1: Conditional Probability Bar Chart
<img width="1190" height="490" alt="image" src="https://github.com/user-attachments/assets/b602e7a2-e424-4fd1-a7e6-71941f77ee33" />
Here, each bar represents one audio feature (energy, danceability, etc.), and its height is the probability that a song is highly popular, 
given that feature is High. The dashed baseline shows the probability of high popularity in the dataset overall (~18.8%). So a green 
bar means that feature is a positive signal — songs that score High in it are more popular than average — and a red bar means the opposite. 


Figure 2:
<img width="852" height="590" alt="image" src="https://github.com/user-attachments/assets/81ebb7e5-c7ba-4dfb-b09e-c828604f7375" />
Ideally we want rules in the top-right corner (common and reliable) with warm colors (high lift). Notice the lift values are all pretty close to 1.0, 
which visually reinforces that audio features aren't strong popularity predictors.


Figure 3:
<img width="787" height="690" alt="image" src="https://github.com/user-attachments/assets/55efd990-7754-4f5f-9a93-0f24dbe3ac79" />
This show the 10 best rules and puts support, confidence, and lift side by side for easy comparison (darker blue = higher value). 
Note how often short duration comes up as well as the consequents (things we're predicting) being medium popularity. 


Conclusion: 

Although there aren't any particulary strong signals to indicate high popularity for a song, we can note the recurrence of 
duration=low/short duration of a song for song popularity in general. This could observation could hint to shorter songs 
tending to get replayed more and have lower skip rates. We can also note the fact that in Figure 3, all the strongest antecedents (predictors)
point to medium track popularity. This means we can guess average songs, but not be hits. 

The main conclusion to this is that a tracks popularity likely isn't determined by the features of the track, but external factors instead. 
Things like Artist reputation, exposure, marketing, social media, etc. are more likely to influence a songs popularity than anything found 
in the data. 


Note: 
Potential follow-up could include features like artist follower count, genre trends, or trending audios on social media. 
