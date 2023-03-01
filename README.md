# Data Science Junior Job Market Analysis
The aim of this program was to analyze and visualize the job market for Data Science junior positions in Poland. The data for analysis was collected from four regions - Poland, USA, UK, and German-speaking countries (Germany, Austria, Switzerland) using the Selenium library. The visualization is specific to Poland but is supported by international databases in the categories of required technologies and the number of proposals for data scientists compared to data-related jobs. The collected data underwent cleaning to remove empty and duplicate records (job descriptions).

The program includes preliminary data visualization, and Azure Translator was used to identify the language of the job descriptions and translate them into English. Additionally, NLP techniques were employed by using NER from the Azure environment to analyze job descriptions. The data was prepared for visualization using Tableau software.
# Result of my analysis
![Tableau result](https://github.com/Jkfre247/job-offert-analysis/blob/main/Data%20Science%20Analysis.png)
# Data Collecting
The data was collected from LinkedIn by searching for the phrase "Data Scientist" and selecting the role as a junior in the chosen country. The program undergoes several security measures, from logging in to accepting cookie files. Upon entering the job postings page, the program encounters a page divided into two sections. The left section contains the list of job postings, and the right section displays specific job offer. The program passes through security measures(The page loads only a portion of the job postings, so the program scrolls down a certain element to obtain all job postings.) to display all job postings.  The program then downloads the appropriate job posting blocks. When a specific block is clicked and a specific offert is displayed, the program then downloads information such as the company name, job position, location, job description, etc.

To save time, the program employs a function that checks if the job posting is within our interest. If not, the job posting is skipped, which significantly streamlines the data collection process. The program also includes basic security measures to avoid disrupting the LinkedIn service and to prevent detection. The program uses the function time.sleep, which not only allows the page to load but also provides a small security measure. After going through all available job postings (up to 1000), the program saves the data in a CSV file.
# Data Cleaning
After the data collection, the program reads the collected data and creates three new columns - country, region, and city using location column. Program fixed broken records that have incorrect data, such as Great Britain, Londyn, Londyn to Great Britain, England, Londyn. The program removes duplicates by looking at the "Description" column. While my initial idea was to have only one job posting per company, I realized that companies could have multiple departments, such as one focused on NLP and another focused on a different area. Therefore, I decided to remove duplicates based on job descriptions to avoid repeated job postings. The program then removes empty rows.

Some job postings from the USA included salary information, which was not present in job postings from other regions. This caused issues with the "Level" and "Type" columns, so the program repaired these cells. Additionally, the program fixed several location-related records.

The program categorizes the databases into four categories - Data Scientist, Data Analyst, AI, and ML - and removes duplicates again to account for the same job posting appearing in multiple countries. The cleaned data is then saved.
# Preliminary Data Visualization

# Language Identification and Translation
# NLP Analysis
# Data Preparation for Visualization
