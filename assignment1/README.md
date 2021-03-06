# Journalists Killed Dataset

## Topic
The death of Washington Post columnist Jamal Khashoggi in Saudi consulate in Istanbul has aroused the public concern for the safety of journalists working in authoritarian states. Based on the "Journalists Killed" dataset by Committee to Protect Journalists, we can look into ：
1. Which country is the most dangerous for journalists?
2. Where were those journalists from? Did they die in their own country or somewhere else? Were they freelance or regular staff? What topics they reported in their daily work? How many of them were male and female? etc.

## Data Source
The dataset contains the basic information of each reporter killed since 1992, including their names, organizations, location of death, etc. You can check the link below:  
https://cpj.org/data/killed/?status=Killed&motiveConfirmed%5B%5D=Confirmed&type%5B%5D=Journalist&start_year=1992&end_year=2018&group_by=year

## Data Field
date - string e.g. April 30, 2018  
location - string e.g. Blida, Algeria  
name - string e.g. Abdel Karim al-Oqda  
organization - string e.g. Algerian Television (ENTV)  
type of death - string e.g. Crossfire  
url - string e.g. https://cpj.org/data/people/abadullah-hananzai/index.php

## Data Volume
1324 rows × 6 columns
The data volume I have finally got is exactly the number of items shown in the dataset website

![a](https://github.com/kaiwenxu94/images/blob/master/Capture.PNG)

## License
CC4.0

## Obstacles and Solutions
As I scraped the information page by page, python reported error *element is not attached to the page document*. I solved the problem by increasing the duration time in time.sleep() and allowing the python to have sufficient time to scrape each page before it clicked "next page" automatically. However, it is time-consuming.  
In addition, there is a small error that is shown after scaping. In the last page(page 67), there is no "next" button, so after python scaped all the data in page 67, it could not find the "next" button, and Python reported the error below:

![a](https://github.com/kaiwenxu94/images/blob/master/Capture1.PNG)

Even though the final result is correct, I think my code in the final part could be refined as follows:

![a](https://github.com/kaiwenxu94/images/blob/master/Capture2.PNG)

## Future Work
Explore and scrape the detailed personal information contained in the "url" section and add more data fields, including their gender, job, beats covered and so on and so forth. 
