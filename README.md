# Data3406 Assignment 2
## Topic: Truth decay

- The problem: This topic aims to quantify the prevalence of misinformation spread on the web due to junk/questionable science.
- Why it matters: People should be able to clearly recognise when online news is based on academic papers that have been retracted

## Driving question

> Q3: Which platforms (various news media, blogs, social media) are common in the dissemination of original papers vs retractions?


The retraction notices are aimed to prevent spreading misinformation, however, people who post may not be aware of, and these cognitive delays will bring truth decay. We are motivated to find which platforms are less common in the dissemination of original and retracted papers, and hopefully the stakeholders will gain benefits from the results and have fewer risks of reading and spreading the fake information.

We tackled this question by comparing information spread on the organization level, that is, the platforms. Specifically, we tracked the references of originals and retractions based on two levels, which are unique user counts and post counts. As a result, the difference of these references of data between original and retractions are visualized to allow people to notice, for example, the platform that has the most posts among the last decade.


## Background

### Data origin

- 26504 retraction notices for 26504 papers
- 106,016 Files, 4 Folders (pubmed id, doi id based original paper and retraction notices)

### Data definitions
The raw data provided is stored in JSON files with an unstructured nature, which means that it does not have a predetermined schema, and it is formatted as key-value pairs and arrays. <br>
The key files we analyze are those with status code 200 from the *doi* folder. There are files with HTTP status code 200 and 404. Code 200 indicates that the body of the response should contain the data requested. Code 404 means that Altmetric does not have any details for the article or set of articles requested, which means there is no valid data within that file. Furthermore, only the data from *doi* are used because we discovered that there are no other changes but only having a variable that is not needed for our research after merging with *pubmed*.

  |    **Key variables**    |                                             **Explaination**                                          |
  | :---------------------: | :---------------------------------------------------------------------------------------------------: |
  |        `pubdate`        |                                      The publication date of the paper.                               |
  |        `counts`         |       A JSON object containing reference data from various platforms. (See two count data below)      |
  |   `unique_users_count`  | A numerical data indicating the number of distinct users mentioned that specific paper in a platform. |
  |      `posts_count`      |      A numerical data indicating the number of posts mentioned that specific paper in a platform.     |

## Getting started

Short list of intructions for new collaborators to get up and running with the project.

1. Make sure the file folder follows below structure: 

- Data3406_shared_data/new_dataset_06_07_2021/original_papers_doi

- Data3406_shared_data/new_dataset_06_07_2021/retracted_papers_doi

And keep the notebook in the same working directory as the file folder.

2. Example list of commands for getting started:

- `$ git clone git@github.com:Bloombergchu/Platform_Dissemination.git`

- `$ pip install -r requirements.txt`


