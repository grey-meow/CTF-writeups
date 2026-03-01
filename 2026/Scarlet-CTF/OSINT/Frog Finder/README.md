# Frog Finder

## Challenge
<img src="Frog_Finder_challenge.png" width="400">

## Challenge Description: 

The challenge mentions that it is located in the ScarletCTF Discord server. This suggests that the flag has something to do with staff or moderators in the server that uses frog-themed profile pictures.

This narrows down the investigation to identifiable frog characters rather than arbitrary usernames or random imagery.

## Suspect Profiles:

Profile 1:

<img src="Frog_Finder_Profile1.png" width="200">

Profile 2: 

<img src="Frog_Finder_Profile2.png" width="200">

## Observation:

-**Profile 1**: Frog character resembles Keroppi (Sanrio)

-**Profile 2**: Unknown frog-related character. A potential lead.

Since profile 1 character does not have a clear in-universe indicator of "wealth", profile 2 is more likely to contain clearer indicator of "wealth" relevant to the frog.

This suggests reverse image search as the next step.

## Reverse Image Search

From the google reverse image search of the frog from profile 2, the reddit post below revealed that the frog came from:

**Lufia II: Rise of the Sinistrals (1995 SNES RPG)**

<img src="Frog_Finder_Reddit1.png" width="200"> <img src="Frog_Finder_Reddit2.png" width="200">

This confirmed the frog was a specific in-game character, shifting the investigation toward in-game attributes rather than community usernames or Discord metadata.


The character is identified as :

```
King Frog
```

Thus, the first half of the flag is:

```
KINGFROG
```

## Determining the "wealth" of King Frog

I searched online and found out that King Frog it is labelled as "normal enemy". In RPGs, enemy “wealth” is typically reflected by the gold reward obtained after defeating them:

<img src="Frog_Finder_search1.png" width="200">

500 gold

Attempted flag:
```
RUSEC{KINGFROG_500}
```
This was incorrect, indicating the value required more precise verification. Now the actual gameplay must be reviewed for the actual value of gold 

## Gameplay Analysis

To verify the actual gold value, gameplay footage was reviewed:

Youtube reference:
[Lufia II: Rise of the Sinistrals](https://youtu.be/uF6F3XtEUCk?si=UDr9F67XefoClB77).

Observed values:

When the player defeated 1 snell and 2 King Frog: the user received 1032 gold [timestamp: 7:01 - 7:32]

When the player defeated 2 snell and 2 King Frog: the user received 1364 gold [timestamp: 8:08 - 8:58]

### Mathematical calculation

Assuming gold rewards are additive with no modifiers applied:

```
1 snell = 332 gold

2 King Frog = 1032-332 = 700 gold

1 King Frog = 700/2 = 350 gold
```
Therefore:
```
1 King Frog = 350 gold
```

## Final Flag
```
RUSEC{KINGFROG_350}
```
