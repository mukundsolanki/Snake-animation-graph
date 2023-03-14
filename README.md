  ![Snake animation](https://github.com/mukundsolanki/mukundsolanki/blob/output/github-contribution-grid-snake.svg)

# Snake-Animation-in Profile Readme

Okay, so you came across my profile and saw that cool Snake Animation of my Contribution graph & and you thought how can i implement it? right? here's how...



## Step 1

Create a repository with your username (the exact one you use). Github will tell you that the file created is special and that everything you add to it will appear in your profile. Make sure it’s public and initialize it with a README to get started.

## Step 2

replace (username) to your Github username
and paste it in your Readme.md file

```bash
  ![Snake animation](https://github.com/(username)/(username)/blob/output/github-contribution-grid-snake.svg)
```
    
## Step 3

Copy all the code given below...

```bash
  name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v2
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v2.6.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Step 4
Go you your tab Actions in your README repository and create a New Workflow. This will generate a new folder in your repository called .github/workflows and a new file inside of it called Create main.yml or main.yml.

## Step 5
Delete everything inside the newly created file Create main.yml or main.yml , and paste the code you copied in Step 4 from my Create main.yml file.

## Step 6
Substitute my username to yours in github_user_name : ( your_username )

## Step 7
Now go to View runs an click on Run workflow . Your contribution graph will update every 12 hours. You can change it in the code in your .ymlfile.

And that is it!
