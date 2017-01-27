# Anime-Recommender
A K-Means clustering anime recommender written in Python.

As an avid anime watcher, one of the main problems I have is to add anime series that
I'm interested in to my backlog. It is a problem of choice: there are so many anime 
shows that it is very difficult to choose one. I'm sure I'm not the only one with this problem.

However, it is quite possible that there are some patterns in the anime series anyone like
to watch, such as genres, length and so on. For example, if someone likes Action and Mecha anime,
it is unlikely he will watch a Shoujo anime and vice versa.

This code uses K-Means clustering with genres only, and will take anime IDs and ratings as inputs. 

It is designed to be done in batch, such as with the rating.csv file given in the data set.

Input:

Anime.csv

    anime_id - myanimelist.net's unique id identifying an anime.
    name - full name of anime.
    genre - comma separated list of genres for this anime.
    type - movie, TV, OVA, etc.
    rating - average rating out of 10 for this anime.
    members - number of community members that are in this anime's "group".

Rating.csv

    user_id - non identifiable randomly generated user id.
    anime_id - the anime that this user has rated.
    rating - rating out of 10 this user has assigned (-1 if the user watched it but didn't assign a rating).

Output:

result.csv

    Rating ID - same as the user_id in Rating.csv
    Name - full name of the recommended anime
    Genre - comma separated list of genres for this anime
    Kind - movie, TV, OVA, etc.
    Episodes - number of episodes of the anime
    
It should be noted that only 5-6 animes will be produced by each user.
