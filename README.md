<H3>ENTER YOUR NAME : Gayathri A</H3>
<H3>ENTER YOUR REGISTER NO. 212221230028</H3>
<H3>DATE:</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
  
Perform sentiment analysis using your Facebook data and filter the data that has only Positive feedback for the code given in the following link.

<H3>Program:
  
```
  pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with positive sentiment (label 'P')
positive_feedback = df[df['Label'] == 'P']

# Output the negative feedback
print(positive_feedback)
```
<H3>Output:</H3>

![image](https://github.com/Gayathriraj18/Project-Based-Experiment-AAI/assets/94154854/a5ba402e-8434-4598-a1fa-690abaa6c604)

<H3>Inference:</H3>

Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
