# PanicAtTheSchool
CAPP 30122 Group Project: 
Sarah, Eshan, and Amari


Our aim of this project is to assess factors which may be contributing to low attendance rates in Chicago public high schools. Based on attendance data from Chicago Public Schools (CPS), grades 9-12 show the lowest attendance rates of all grade levels in the last decade, at an average of about 86.51% before 2019. Moreover, there was a noticeable drop in attendance post-COVID, with high school atteandance rates falling to an average of about 78.79% in school years 2021 and 2022 following the pandemic. 

In our investigation we used CPS data (cps.edu), an API through the Chicago Data Portal, and other publically available data sources to investigate factors in attendance. We have broken down our study into two main focus areas: the relationship between school misconducts and community crime rates as an influence on the criminalization of students (which we hypothesized may be associated with changes in attendance), and the impact of COVID in schools. 

During this process, we used pandas to clean our data, plotly to create data visualizations, and dash to launch our web page/application. While further analysis (which goes beyond the scope of this project) would be necessary to truly determine what plays a role in attendance, we were able to find pretty interesting results that could lead to future research opportunities. 

To see our findings, run the following commands within the cloned PanicAtTheSchool repository in your VSCode terminal:


1. ~/PanicAtTheSchool$ poetry install
2. ~/PanicAtTheSchool$ poetry shell
3. ~/PanicAtTheSchool$ pip install pyjarowinkler
4. (in the shell) ~/PanicAtTheSchool$ python3 -m CAPP_project
5. From here, you can choose to directly launch the dash app by entering '1', or you may examine each step in the data pipeline by entering '2.'
6. If you choose '1', select the pop-up message "Open in Browser" appearing on the bottom right of the screen to launch the web page.
7. If you choose '2', you have several options:
    - fetch: runs the API data collection process to create or update our crime.csv
    - clean: loads in our data sets, filtering and managing unusal or unknown values
    - merge: loads in our cleaned data sets, and merges them for further analysis and plotting. 
    - exploratory: fetches teacher and mobility, matches with school data using Jaro-Winkler and merges files; this data is not used for final analysis 
    - plot: runs all the code to create visualizations 
    - all: runs the entire data pipeline, cleaning, merging, plotting and ultimately launching our Dash appplication.

Note 1: Pulling data from the Chicago Data Portal API (as would happen if you selected 'fetch' or 'all') requires a private token to be assigned to TOKEN at line 16 of the 'crime_api.py' file, instead of using the environmental variable as discussed in class. Professor Turk has been provided this private token for grading purposes. Pulling this data takes approximately 10 minutes.

Note 2: If you do not wish to pull data from the API or have not been given the private token, you can access the static crime data file at the below link. This file can be downloaded as a csv at the link, placed in the 'CAPP_project/raw_data' subdirectory, and renamed 'crime.csv.'

Link to crime csv.
https://uchicago.app.box.com/file/1154307867116?s=3tpb8dibaad6i1usrc5dr96cymzdv7m4

8. When you have fully explored the webpage and are back in your terminal, run ctrl+c to close the application.
