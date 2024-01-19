# YouTube Watch History Analysis

## Overview
This project involves analyzing your YouTube watch history using the YouTube Data API v3. It includes retrieving video details, creating visualizations, and building a machine learning model to predict whether you are subscribed to the channels of the watched videos.

## Project Structure
1. **Authentication:** The `authenticate()` function in the script is used to authenticate and obtain credentials for accessing the YouTube Data API.

2. **Video Retrieval:**
    - The script fetches video details from your watch history playlist, including video ID, publish date, channel title, tags, categories, duration, view count, like count, comment count, and topic categories.
    - Video details are stored in a DataFrame and can be exported to a CSV file.

3. **CSV Creation from HTML:**
    - Parses an HTML file containing YouTube watch history to extract video IDs.
    - Creates or updates a CSV file with unique video IDs.

4. **Video Details from CSV:**
    - Retrieves video details from the YouTube API using video IDs from the CSV file.
    - Converts the results into a DataFrame.

5. **Data Cleaning and Transformation:**
    - Converts count columns to numeric.
    - Converts video duration to seconds.
    - Removes rows with both like_count and comment_count values equal to 0.

6. **Exploratory Data Analysis (EDA):**
    - Visualizes video views using bar plots.
    - Explores videos with longer durations.
    - Analyzes the number of appearances of favorite channels.
    - Explores the distribution of log-transformed view counts.
    - Explores the relationship between log-transformed view counts, comment counts, and like counts.
    - Creates a word cloud of video tags.

7. **Machine Learning Model:**
    - Predicts whether a user is subscribed to a channel based on video features.
    - Uses a Random Forest Classifier.
    - Evaluates model performance with cross-validation, accuracy, confusion matrix, and classification report.
    - Provides a heatmap visualization for the confusion matrix.

8. **README.md:**
    - This file provides an overview of the project, its structure, and a guide on how to use and understand the script.

## How to Use
1. **Authentication:**
    - Replace `CLIENT_ID` and `CLIENT_SECRET` with your YouTube Data API credentials.
    - Update the path to your `client_secret.json` file.

2. **CSV Creation from HTML:**
    - Replace `html_file_path` with the path to your YouTube watch history HTML file.
    - Replace `csv_file_path` with the desired path for the CSV file.

3. **Video Details from CSV:**
    - Replace `csv_file_path` with the path to your CSV file.

4. **Machine Learning Model:**
    - Ensure you have the required libraries installed (`pandas`, `numpy`, `scikit-learn`, etc.).
    - Update the paths for the CSV file and adjust parameters as needed.

5. **Run the Script:**
    - Execute the script in a Python environment.

## Dependencies
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `google-auth-oauthlib`
- `google-auth-httplib2`
- `google-api-python-client`
- `isodate`
- `beautifulsoup4`
- `wordcloud`

## Acknowledgments
- This project uses the YouTube Data API v3.
- Special thanks to the developers of the libraries used in this project.

Feel free to contribute, report issues, or suggest improvements. Happy coding!
