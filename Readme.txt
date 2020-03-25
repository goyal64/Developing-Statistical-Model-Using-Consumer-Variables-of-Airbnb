Steps to Reproduce:

Python
1. Download the dataset from the source https://www.kaggle.com/airbnb/seattle
2. Import the listing dataset to pandas dataframe
3. Import the reviews data to pandas dataframe
4. Clean the listing dataset and remove unwanted columns
5. In the reviews dataframe, convert all the reviews to string format
6. Remove reviews which have a length of less than 3 to avoid single word or random comments
7. Using Langdetect, detect the language of the reviews and keep only the reviews supported by Google NLP
8. Reindex the dataframe to avoid missing indices
9. Using Google NLP package, generate sentiment scores for all the reviews. While generating the score, after every 500 reviews set a timer sleep for 60 seconds to avoid Google interrupting the code due to requests per minute restriction of 600 per minute.
10. Add the sentiment score to the reviews dataframe and generate a average score by listing id.
11. Merge the 2 dataframes by Listing id
12. Data cleanup: Converting price, security deposit, cleaning fee, extra people to float values
13. Generate a final excel sheet of the resulting dataframe and export the csv to Minitab to run the regression.

Minitab:
1. Upload the file from above steps in minitab
2. Run a regression analysis including second order interaction terms