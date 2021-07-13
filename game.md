<frontmatter>
  header: header.md
  pageNav: 2
  pageNavTitle: "Game Development Guide"
  siteNav: site-nav.md
  footer: footer.md
</frontmatter>

<br>

<div class="jumbotron jumbotron-fluid bg-dark text-white">
  <div class="container">
    <h1 class="display-4 no-index">In My Shoes</h1>
    <p class="lead">Development Guide</p>
  </div>
</div>

# Introduction

The game consists of the following components:
- The web application that renders the game content and handles the game logic. This should be updated by a programmer, when there is a need to make modifications to the game.
- The media resources that include images and videos. This is uploaded in DigitalOcean's storage space. They are typically separated by game and should follow the existing folder structure when adding a new set of game media assets for a new game.
- The JSON file that specifies the game content for each version of the In My Shoes game. This should be updated by game content in-charge to ensure all textual information is up to date. The structure of the file must be followed and the convention used must not be violated in order to run the game successfully.

For future additions of a game, given that the general settings/game logic does not deviate from existing setup, a game content in-charge can upload relevant media assets and fill in the JSON file for the new game content, then he/she will be able to generate a new set of game.

---

# Game state
Consists of
- welcome (Greeting page, says what game this is)
- pregame survey (Form to find out age group etc)
- intro (Few slides on the game introduction)
- character selection (Shows all available characters)
- character information (Shows the selected character details)
- story (Shows a series of scenarios)
- wildcard (When triggered during story)
- credit (ending page, allow for 'play again', feedback form)
- postgame survey (enter from credit page)

---

# Game JSON file
Consists of
- welcome
- intro
- characters
- wildcards
- credits

## welcome
Specifies the name of the game, this is shown on the first page of the game.

## intro
Specifies the slides of the introduction that follows right after the pre game survey. Use of HTML syntax such as `<b> <br> <small>` is allowed for additional styling to bold, make line break, or make smaller. Background image is used on the content box.

## characters
Keeps a list of characters, they are make of profile details and also the story of the character. The story lists out each scenario and what outcome is linked. The story always start with first node having id of 1. The updateState field keeps track of the numerical update to the meter values. The wildcards that are application to the character is also explicitly stated.

## wildcards
Keeps a list of descriptions for all wildcards available for that particular game.

## credits
Allow for additional logo or textual copy right information to be included for that particular game.

---

P.S.
Stuff that I need your help to fill in
- how to upload resources
- how to organize the file structure and naming
- some details for the above JSON files
- any other things u know when u edit the file that someone who will take over this should know...

# Uploading Resources
All images and videos files are to be uploaded onto https://cloud.digitalocean.com/spaces/soristic?i=099850&path=pwd%2Fthomas%2F via soristic.asia email account. The files can be found under Spaces. Next, click onto the space titled ‘soristic’, and the respective game folders are found. Click onto the respective game folders to upload the files accordingly. 

## In each game folder
Consists of
- ‘character’s name’ folder
- ‘character’ folder
- ’videos’ folder
This is compulsory for all games. 

This is in the existing Youth and Senior games. Unless new games require new images for the following categories, else can reuse the images stored in the following folders
- ‘intro’ folder
- ‘credits’ folder
- ’wildcard’ folder


## ‘character’s name’ folder
Keeps a list of images with regards to the story lines. Each story line has 2-3 choices, each with image icon, e.g. Q1C1 stands for Question 1 Choice 1. Each choice has 1-3 outcome images, e.g. Q1C1R1, stands for Question 1 Choice 1 Row 1. For choices with 3 outcome images, e.g. Q1C1, the images attached are Q1C1R1, Q1C1R2 and Q3C1R3, displayed from left to right on the game app. 

## ‘character’ folder
Keeps a list of game characters’ images, saved in PNG format, under their respective names. E.g. Arthur.png for Arthur in the Youth game.

## ’videos’ folder
Keeps a list of introduction videos of each character, saved in mp4 format, under their respective names. E.g. Arthur.mp4 for Arthur in Youth game. 

## ‘intro’ folder
Keeps a list of images used in the introduction of the game. 

## ‘credits’ folder
Keeps a list of images used in the ending page of the game. 

## ’wildcard’ folder
Keeps a list of background images of the respective wildcards.