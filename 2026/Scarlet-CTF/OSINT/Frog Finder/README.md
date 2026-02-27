# Frog Finder

## Challenge
<img src="Frog_Finder_challenge.png" width="400">

## Challenge Description: 

The challenge mention that it's in ScarletCTF Discord server. This suggests that the flag has something to do with staff or moderators in the server that have frog-related character as their profile pictures.

--

## Suspect Profiles:

Profile 1:

<img src="Frog_Finder_Profile1.png" width="200">

Profile 2: 

<img src="Frog_Finder_Profile2.png" width="200">

## Observation:

-**Profile 1**: Frog character resembles Keroppi (Sanrio)
-**Profile 2**: Unknown frog-related character. A potential lead.

Reverse image search is required to identify profile 2. 

--

## Reverse Image Search

From the google reverse image search of the frog from profile 2, the reddit post below revealed that the frog came from:

**Lufia II: Rise of the Sinistrals (1995 SNES RPG)**

<img src="Frog_Finder_Reddit1.png" width="200"> <img src="Frog_Finder_Reddit2.png" width="200">
 --

The character is identified as :

```
King Frog
```

Thus, the first half of the flag is:

```
KINGFROG
```

---

## Determining the "wealth" of King Frog

I searched about King Frog and found out that it is labelled as "normal enemy". Usually in games if you kill enemies you will get rewarded. Based on that, the "wealth" of King Frog could translate to how much reward you will get from killing one King Frog. Here's what came up:

<img src="Frog_Finder_search1.png" width="200">

500 gold. Let's try that flag. 

RUSEC{KINGFROG_500}

It seems like that is not the flag. Now I have to actually see the gameplay. 

I searched up on youtube; "Lufia 2: Rise of the Sinistrals King Frog". Here's the link to the [video](https://youtu.be/uF6F3XtEUCk?si=UDr9F67XefoClB77).
The game gives the total amount of gold after killing the enemies. Seems like some math needs to be done.

When the user killed 1 snell and 2 King Frog, user received 1032 gold [timestamp: 7:01 - 7:32]

When the user killed 2 snell and 2 King Frog, user received 1364 gold [timestamp: 8:08 - 8:58]


1 snell = 332 gold

2 King Frog = 1032-332 = 700 gold

1 King Frog = 700/2 = 350 gold


The final flag is:

RUSEC{KINGFROG_350}
