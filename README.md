# PS239T-Final-Project
#### Jiali Li
#### April 25, 2018
 
## Short Description

My PS239T final project focused on collecting descriptive data and producing visualizations of China's nightly news, Xinwen Lianbo (xwlb). xwlb is the most viewed tv news program in China, and one of the fundamental propaganda tools for the Chinese government. This project peeks into the content of the program in the past two years (2016-2017) and aims to uncover some patterns. I used Python to scrape the transcripts of the program from 2016 to 2017, and created several labels of interest. The unit of analysis is the individual segments of the daily broadcast. I then visualized the variation in mentions of the top leadership of the regime, and across all the provinces. Lastly, I used topic modeling to identify the topic keywords and found some interesting patterns. 

## Dependencies

My code depends on the following software:
R, version 3.4.3
Python version 3.6.3, Anaconda 4.5.1

## Files

This provides a list of all files contained in the repo, along with a brief description of each one:

**data**

1_xwlb_content_title_daily.csv: Contains the data, with colomns content, date, and title. The content column includes individual paragraphs; the date column indicates the respective date of broadcast; and the title column indicates the title of each segment. Each segment may have multiple paragraphs, and each date may have multiple segments.

2_xwlb_content_title_daily_labeled.csv: contains the first dataset and some new labels, including the day of the week, whether the segment mentions Xi Jinping, whether the segment mentions Li Keqiang (PM), and whether the segment includes weather.

3_xwlb_daily_province_mentions.csv: Contains the count of segment mentions for the provinces.


**code**

01_Webscraping.ipynb: Collects data from http://mrxwlb.com/ and exports the data to the file 1_xwlb_content_title_daily.csv

02_analyses_and_visualization.ipynb: Conducts descriptive analysis of the data, producing the visualizations (graphs and maps) found in the results directory.

03_text_analysis.ipynb: Conducts text analysis of the data, producing the topic modeling results for the weekday set of data, the weekend set of data, and the entire dataset.


**results**

result1_xwlb_daily_XJP_mentions: Graphs the number of Xi Jinping mentions.

result2_xwlb_daily_province_mentions.png: Maps the mentions of provinces, with red as the most mentions and light blue as the least. The varying shades show that the coastal area have been mentioned more frequently than any other area. Be

result3_xwlb_daily_weekend_topics.csv: Topic keywords from weekend xwlb articles, in Chinese.

result4_xwlb_daily_weekday_topics.csv: Topic keywords from weekday xwlb articles, in Chinese.

result5_xwlb_daily_weekday_topics_eng.csv: Topic keywords from weekend xwlb articles, in English. Each topic has a manually determined label, based on the keywords.

result6_xwlb_daily_weekend_topics_eng.csv: Topic keywords from weekday xwlb articles, in English. Each topic has a manually determined label, based on the keywords.

result7_xwlb_daily_all_topics.csv: Topic keywords from all the xwlb articles, in Chinese.

result8_xwlb_daily_all_topics_eng.csv: Topic keywords from all the xwlb articles, in English. Each topic has a manually determined label, based on the keywords.


**More Information**

Since many of the output files are in Chinese (or partly in Chinese), you may encounter encoding issues when opening them. One way to open the .csv file in Microsoft Excel is to follow the procedures below:
- Open Excel
- Go to Data
- Go to From Text
- Select Delimited
- Select File origin: 54936: Chinese Simplified (GB18030)
- Select My Data has headers
- Select Deliminaters: Comma
