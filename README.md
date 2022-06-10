# TechAssesment
Maximum no. of video plays, playing concurrently


Find the maximum number of video plays that were playing concurrently.

# Assumptions
I made some assumptions for the task:

- Start and end times are in Epoch time.
- Data is stored in a csv file - in reality I'm guessing this would be a database or something similar.
- Videos that start on the exact second that another video ends counts as a concurrent video play.

# Method
- Load data from csv file
- Label start and end times with "start" and "end" respectively
- Sort times in ascending order, making sure start times appear in list before end times to account for videos which start and end at the same point in time
- Loop through sorted times, if a time is marked as "start" then add 1 to the counter, if "end" then subtract 1 from the counter.
- Whilst looping through sorted times, check to see if current counter value is the maximum value. Set maximum value to counter value if the counter value is higher  than the current maximum value.
- Return maximum value

# Solution

The code is in the max_concurrent_videos.py file, I have created a data file video_plays_data_1000000.csv using the code datafile_create.py

# Data Prep

Run the code datafile_create.py to create a csv file with mock up data

# Code Execution
```
python max_concurrent_videos.py video_plays_data_1000000.csv
```
