<p align="center">
  <img src="Generic-FTR-headers_V10-1920x733.jpg" alt="Alt text" width="900"/>
</p>

# Sentiment Analysis of Spotify Reviews

This project analyzes user reviews of the Spotify app using Natural Language Processing (NLP) and Machine Learning (ML). The dataset contains user feedback labeled as either **POSITIVE** or **NEGATIVE**, and the goal is to classify sentiments and gain insights into user opinions about Spotify.

## Table of Contents
- [Installation](#installation)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Visualizations](#visualizations)
- [Model Evaluation](#model-evaluation)
- [Insights](#insights)
- [Contributing](#contributing)
- [License](#license)
---

## Installation
To run this project locally, make sure to install the required Python libraries:

```bash
# Install required libraries
pip install wordcloud nltk
pip install kaggle
pip install pandas matplotlib seaborn scikit-learn
```

Additionally, download the NLTK stopwords:
```
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

## Dataset
- **Source**: [Spotify Dataset on Kaggle](https://www.kaggle.com/datasets/alexandrakim2201/spotify-dataset)
- **File Used**: `spotify.csv`
- **Dataset Info**:
  - 52,702 rows, 2 columns: `Review` (text data), `label` (sentiment: POSITIVE or NEGATIVE).
  - Missing values handled during preprocessing.

---

## Project Workflow
### 1. **Data Preprocessing**
- **Lowercasing**: All text was converted to lowercase.
- **Removing Missing Values**: Rows with missing reviews were removed.
- **Cleaning Text**: Removed punctuation, numbers, and stopwords using NLTK.

### 2. **Exploratory Data Analysis (EDA)**
- Distribution of sentiments visualized using bar plots.
- Word clouds generated for positive and negative reviews.

### 3. **Modeling**
- Split data into train and test sets using an 80-20 ratio.
- **TF-IDF Vectorization**: Converted cleaned text to numerical features.
- **Logistic Regression**: Trained on TF-IDF features to classify reviews.

### 4. **Evaluation**
- **Classification Report** and **Confusion Matrix** were used to assess the model's performance.
## Visualizations

### Sentiment Distribution
- Bar plot showing the distribution of positive and negative sentiments.

---

### Word Clouds
#### Positive Reviews
- Word cloud generated from positive reviews to visualize frequent words.

#### Negative Reviews
- Word cloud generated from negative reviews to visualize frequent words.

---

## Model Evaluation

### Classification Report:

| Metric      | NEGATIVE | POSITIVE | Average |
|-------------|----------|----------|---------|
| Precision   | 0.89     | 0.88     | 0.88    |
| Recall      | 0.91     | 0.85     | 0.88    |
| F1-Score    | 0.90     | 0.87     | 0.88    |
| **Accuracy**| -        | -        | **88%** |

---

### Confusion Matrix:

|                | Predicted NEGATIVE | Predicted POSITIVE |
|----------------|--------------------|--------------------|
| Actual Negative | 5864               | 585                |
| Actual Positive | 701                | 3973               |

## Insights

- **Positive Reviews**: Users appreciated features like playlists, offline mode, and audio quality.
- **Negative Reviews**: Common issues included ads, bugs, technical problems, and dissatisfaction with updates.
- **Overall Sentiment**: While positive reviews are slightly higher, the significant proportion of negative feedback indicates areas for improvement.

## Contributing

Contributions are welcome! If you'd like to improve this project:

---

## License

This project is licensed under the MIT License. See the [LICENSE.md](LICENSE.md) file for details.
