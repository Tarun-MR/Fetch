# Offer Recommendation Dashboard

## Introduction

This Python script, `final.py`, implements an offer recommendation dashboard using Dash, a Python framework for building analytical web applications. The dashboard recommends offers based on user input and utilizes natural language processing (NLP) techniques.

## Approach

In addressing the challenge of enabling intelligent offer searches through text input, a multifaceted approach was taken with a primary focus on simplicity, efficiency, and user experience. The following summarizes the key aspects of the approach:

### Assumptions

1. **Text Preprocessing:** Robust text preprocessing, including lemmatization, stop-word removal, and tokenization, is crucial for accurate similarity measurements.

2. **Similarity Score:** A combination of basic text similarity via difflib's SequenceMatcher and a more advanced TF-IDF approach is used to balance accuracy and computational efficiency.

3. **Keyword Extraction:** Extracting keywords from user input and offer descriptions enhances relevancy assessments. The chosen CountVectorizer method is straightforward for simplicity.

4. **Duplicate Removal:** Eliminating duplicate offers with higher similarity scores improves user experience by providing concise and relevant recommendations.

5. **User Interface:** The Dash web application provides a clear and interactive interface for users to input queries and receive offer recommendations.

### Trade-offs

1. **Complexity vs. Performance:** Algorithmic complexity is traded off to maintain performance, prioritizing a solution that remains computationally efficient, especially in a real-time application.

2. **Threshold for Duplicate Removal:** The duplicate removal threshold is set at a similarity score of 0.8, involving a trade-off between precision and recall.

3. **Keyword Extraction Method:** CountVectorizer is chosen for its simplicity, with potential exploration of more advanced methods in the future.

4. **User Interaction:** The web app interface is intentionally kept minimalistic for ease of use, balancing simplicity and functionality.

### Prompt Engineering Consideration

While prompt engineering for semantic understanding was considered, the decision was made to prioritize the current implementation due to computational intensity concerns, ensuring a balance between accuracy and response time.

### Future Consideration

Given the opportunity, there is interest in exploring a more computationally intensive implementation with advanced NLP models like BERT for richer semantic understanding and even more precise recommendations. Collaboration is welcomed to refine and expand the tool based on evolving requirements.

## How to Run

1. Open your terminal in the directory containing `final.py`. If you are using Jupyter Notebook, navigate to the directory using the following commands:

    ```bash
    cd Documents/Fetch
    ```

2. Run the `final.py` script:

    ```bash
    python final.py
    ```

3. Open your web browser and navigate to [http://127.0.0.1:9010/](http://127.0.0.1:9010/) to access the Offer Recommendation Dashboard.

## Code Explanation

The script performs the following tasks:

1. **Package Installation:** Installs or upgrades necessary Python packages using the `pip` command.

2. **Imports:** Imports required libraries and modules, including Dash, pandas, scikit-learn, NLTK, and others.

3. **NLTK Data Download:** Downloads essential data for Natural Language Toolkit (NLTK).

4. **Dash App Initialization:** Initializes the Dash app with the Bootstrap theme.

5. **Text Processing Functions:** Defines functions for text processing, similarity score calculation, and recommendation generation.

6. **Data Loading:** Loads data from CSV files using pandas and merges relevant dataframes.

7. **Dash Layout Definition:** Defines the layout of the Dash app, including input fields, buttons, and output display.

8. **Callback Function:** Defines a callback function to update the output display based on user input.

9. **Data Preprocessing:** Preprocesses the loaded data by tokenizing, lemmatizing, and combining relevant text columns.

10. **TF-IDF Vectorization:** Uses TF-IDF vectorization to convert text data into numerical vectors.

11. **Server Initialization:** Runs the Dash app server on a specified host and port.

## Usage

1. Enter a search query in the provided input field.

2. Click the "Submit" button to trigger the recommendation generation.

3. View the recommended offers and their similarity scores in the output section.

## Walkthrough 


There is a walkthrough video in the repository. It is named Walkthrough.mp4. Visit it to see how i run this code.

## Troubleshooting

If there are issues running the script, ensure that the required CSV files (`offer_retailer.csv`, `brand_category.csv`, and `categories.csv`) are present in the specified file paths.

In case of file not found errors, check and provide the correct file paths.

## Troubleshooting - Changing Server Configuration

If you encounter issues, mostly due to hosting on the same server, consider changing the server configuration in the last part of the code. Modify the `host` and `port` variables in the following section of the code:

```python
port = 9030  # Change port if there is a connection issue
print(f" * Running on http://{host}:{port}/ (Press CTRL+C to quit)")
app.run_server(debug=True, port=9030)

