# Hotel Review Analysis

## Project Overview
Customer reviews provide valuable insights into user satisfaction and areas needing improvement. This project focuses on analyzing **negative hotel reviews** from the [TripAdvisor Hotel Reviews dataset](https://www.kaggle.com/datasets/andrewmvd/trip-advisor-hotel-reviews). By leveraging **Natural Language Processing (NLP)** and **clustering techniques**, the goal was to uncover recurring themes in the negative reviews and categorize them into distinct clusters.

---

## Project Workflow

### 1. Data Preprocessing
Using `spaCy`, the following preprocessing steps were applied:
- Removal of URLs and emojis
- Punctuation removal
- Elimination of extra spaces
- Conversion to lowercase
- Lemmatization to extract root words

### 2. Sentiment Analysis
- Applied the `SentimentIntensityAnalyzer` to classify reviews into positive, neutral, and negative sentiments.
- Focused only on **negative reviews** for further analysis.

### 3. Feature Engineering
- Transformed the text into numerical data using `TfidfVectorizer`.

### 4. Clustering
- Determined the optimal number of clusters (`k`) using the `Stellhouse_score` method.
- Applied **K-means clustering** to group the reviews into meaningful themes.

---

## Results
The analysis revealed **three main clusters** of negative reviews:

1. **Cluster 0:** 
   - Topics: Hotel operations, staff service, booking issues
   - Common Words: hotel, room, stay, service, staff, night, check, book, day

2. **Cluster 1:**
   - Topics: Food quality, resort and dining experience
   - Common Words: food, resort, beach, restaurant, bad, people, service

3. **Cluster 2:**
   - Topics: Room issues like cleanliness, maintenance, and size
   - Common Words: room, bed, place, dirty, bathroom, small

---

## Conclusion
The clustering results highlight key dissatisfaction areas for hotel management to address:
- **Customer Service:** Streamline check-in processes and train staff for better service.
- **Food and Dining:** Improve food quality and enhance restaurant experiences.
- **Room Maintenance:** Ensure rooms are clean, well-maintained, and spacious.

By acting on these insights, hotels can improve customer satisfaction, reduce negative reviews, and enhance their overall reputation.

---

## Tools and Technologies
- **Languages:** Python
- **Libraries:** `spaCy`, `NLTK`, `TfidfVectorizer`, `scikit-learn`
- **Clustering Algorithm:** K-means
