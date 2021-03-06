# Football Player Tracking Dataset

This repository holds the annotations we have used for player detection, and player tracking.

It does not hold the raw images, but the instructions to download them are below.

If you are at Oregon State and have access to the vision server, the dataset is currently located under /scratch/datasets/NFL/football_players

## Getting Videos

Download the nflvid python package and follow installation instructions here:

```
https://github.com/BurntSushi/nflvid
```

The NFL does not necessarily support this so at some point they might shut this down. At the time of
building this repository, May 18, 2017, it was still working.

If the project is still operational, now you can download NFL games from the coaches viewpoint!

We used a few specific games from the 2014 season for these annotations:
+ SEA vs SD Week 2
+ DEN at KC Week 2
+ SEA at DEN Week 3
+ NE at OAK Week 3
+ NE vs KC Week 4
+ GB vs CHI Week 4
+ GB at MIN Week 5
+ SEA at DAL Week 6
+ IND vs HOU Week 6


To download them use the command:

```
nflvid-footage --season 2014 --weeks 3 4 --teams NE --threads THREADS /path/to/folder/you/want
nflvid-footage --season 2014 --weeks 2 3 6 --teams SEA --threads THREADS /path/to/folder/you/want
nflvid-footage --season 2014 --weeks 2 --teams DEN --threads THREADS /path/to/folder/you/want
nflvid-footage --season 2014 --weeks 4 5 --teams GB --threads THREADS /path/to/folder/you/want
nflvid-footage --season 2014 --weeks 6 --teams IND --threads THREADS /path/to/folder/you/want
```

Once you have the full games downloaded you will need to use the `nflvid-slice` commnand to split up the full videos into plays.
You can do that with the following commands:

```
nflvid-slice /path/to/playbyplayvideos /path/to/full_games/*.mp4
```

Now you should have all the video information you need for the datasets

## Player and Background Annotations for Player Detection


