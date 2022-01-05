This repository provides the replication package for the paper titled *An Empirical Study on the Survival Rate of GitHub Projects* sent to the *Mining Software Repositories* conference, currently under review.

# Contents

The repository contains all the data required to generate the plot shown in the paper and, thus, come to our conclusions.
In the following, we briefly describe the content of the `data` folder.

## `data`folder

This folder includes the data from our database extracted in CSV files.
There are 5 types of CSV files, each divided by ecosystem:

* `AllData.csv`, which is the data dump from our database.
* `AllData-Month.csv`, which has the events grouped by month.
This file has a few processing from the previous data dump.
The computed attributes are: `act_type`, which classifies the event types as `CODE`, if the event is a commit or a pull request, and `NON\_CODE`, if it is an issue, a comment or a review; `date_month`, which tells the date of the month in the YYYY-MM format; and `activity`, which tells the number of events per repository, event type, user type (whether it is a user or a bot, given by `isbot` column) and date.
* `Chains.csv`, which contains the state chains used in RQ1.
* `metadata.csv`, which, for each repository, has the information of whether it is a repository owned by a user or organization account, the tier of the community size (either 1, 2 or 3), the status at the end of the study (used in RQ2) and the lifespan reported in months.
* `oracle-2016.csv`, which complements `metadata.csv`providing the number of users in the community (see column `Authors`), and the number of project resources created along its lifespan (see columns `Commits`, `Pulls`, `Issues`, `Comments` and `Reviews`).