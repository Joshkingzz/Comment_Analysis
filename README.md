### Description

This Python script processes a dataset of comments to identify and extract relevant information, such as website links, app-related comments, and unique words. The script provides the following functionalities:

1. **Loading and Preprocessing Data**:
   - Reads a JSON file containing comments.
   - Converts data to strings and standardizes column names.
   - Removes whitespace from comments.

2. **Extracting and Filtering Website Links**:
   - Identifies comments containing website URLs using a regex pattern.
   - Saves filtered comments with website links to a CSV file (`Web_comment.csv`).
   - Extracts all unique website links from the dataset and saves them in another CSV file (`only_websites.csv`).

3. **Text Cleaning and Word Extraction**:
   - Joins all comments into a single string, converts to lowercase, and splits into individual words.
   - Removes duplicates and unwanted characters using regex.
   - Extracts words starting with capital letters, sorts them alphabetically, and identifies unique terms.

4. **Identifying App-Related Comments**:
   - Imports a list of app names from a CSV file and checks if each app name appears in any comment.
   - Collects all comments mentioning specific app names and saves them in a new DataFrame.

5. **Filtering Comments Without Website Links**:
   - Removes comments containing both app names and website links.
   - Strips comments to remove excess whitespace.

6. **Additional URL Extraction**:
   - Defines a custom function to extract URLs from comments and creates a new column for extracted URLs in the dataset.

### Files Generated
- `Web_comment.csv`: Comments containing website links.
- `only_websites.csv`: Extracted URLs from the comments.
- `App_df`: Comments mentioning specific app names.
- `Appz_df`: Filtered comments without website links.

### Use Case
This script was used to:
- Analyze large sets of user comments for specific patterns such as app mentions, website links.
- Preprocess and clean text data for further analysis.
- Extract structured information like URLs or keywords from unstructured comment data.

