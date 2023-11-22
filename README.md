# Data Scientist NLP Apprenticeship Take-Home

## Introduction

Welcome to the Fetch Data Scientist NLP Apprenticeship Take-Home project! This assignment involves building a tool that empowers users to intelligently search for offers via text input. The goal is to enhance user experience and provide valuable recommendations for both users and Fetch partners.

## Problem Statement

Fetch provides value to its user base through a variety of active offers in the app. The objective is to enable users to easily seek out relevant offers using a text-based search. This requires building a tool that can intelligently understand user queries and recommend offers based on categories, brands, and retailers.

## Acceptance Criteria

- If a user searches for a category (e.g., diapers), the tool should return a list of offers relevant to that category.
- If a user searches for a brand (e.g., Huggies), the tool should return a list of offers relevant to that brand.
- If a user searches for a retailer (e.g., Target), the tool should return a list of offers relevant to that retailer.
- The tool should also return the score used to measure the similarity of the text input with each offer.

## Solution Overview

### Approach

In addressing the challenge, a multifaceted approach was taken, focusing on simplicity, efficiency, and user experience:

#### Assumptions

1. **Text Preprocessing:** Robust preprocessing, including lemmatization, stop-word removal, and tokenization, is crucial for accurate similarity measurements.

2. **Similarity Score:** A combination of basic text similarity and advanced TF-IDF is used for accuracy and computational efficiency.

3. **Keyword Extraction:** Extracting keywords enhances relevancy assessments using a straightforward CountVectorizer method.

4. **Duplicate Removal:** Eliminating duplicate offers with higher similarity scores improves user experience.

5. **User Interface:** Dash web application for clear and interactive user input and recommendation display.

#### Trade-offs

1. **Complexity vs. Performance:** Maintaining computational efficiency while balancing algorithmic complexity.

2. **Threshold for Duplicate Removal:** A trade-off between precision and recall in setting the duplicate removal threshold.

3. **Keyword Extraction Method:** CountVectorizer chosen for simplicity.

4. **User Interaction:** Intentional minimalistic design for ease of use.

#### Prompt Engineering Consideration

Considered prompt engineering for semantic understanding but prioritized the current implementation for computational efficiency.

#### Future Consideration

Interest in exploring more computationally intensive implementations with advanced NLP models for richer semantic understanding and precise recommendations.

## How to Run Locally

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/yourusername/yourrepository.git
    ```

2. Navigate to the project directory:

    ```bash
    cd yourrepository
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Run the script:

    ```bash
    python final.py
    ```

5. Open your web browser and go to [http://127.0.0.1:9010/](http://127.0.0.1:9010/) to access the Offer Recommendation Dashboard.

## Dependencies

- Dash (version x.x.x)
- pandas (version x.x.x)
- scikit-learn (version x.x.x)
- NLTK (version x.x.x)
- Other libraries specified in requirements.txt

## File Structure

- `final.py`: Main script implementing the offer recommendation dashboard.
- `offer_retailer.csv`: Dataset containing offers and associated metadata.
- `brand_category.csv`: Dataset containing supported brands and their categories.
- `categories.csv`: Dataset containing product categories.

## Walkthrough Video

- [Walkthrough Video](https://github.com/yourusername/yourrepository/Walkthrough.mp4](https://github.com/Tarun-MR/Fetch/blob/main/Walkthrough.mp4))

## Troubleshooting

If you encounter any issues while running the tool, consider the following troubleshooting steps:

1. **Server Configuration:**
   - If you face difficulties, the likely culprit may be hosting on the same server. To address this, contemplate adjusting the server configuration in the final section of the code.
   - Specifically, alter the port value in the "port" variable to any number within the range of 8000 to 12000. Here's the relevant code snippet:

     ```python
     port = 9030  # Adjust the port if connection issues arise
     print(f" * Running on http://{host}:{port}/ (Press CTRL+C to quit)")
     app.run_server(debug=True, port=9030)
     ```

2. **File Paths:**
   - Ensure that the required CSV files (`offer_retailer.csv`, `brand_category.csv`, `categories.csv`) are present in the specified file paths.
   - Check and provide the correct file paths if there are "file not found" errors.

3. **Error Handling:**
   - If you encounter any issues, refer to this troubleshooting section and ensure dependencies are correctly installed.

## Deployment Options

Consider different deployment options, such as deploying on a cloud platform or integrating with an existing system.

## Acknowledgments

We acknowledge the contributions of third-party tools and libraries used in this project.

## Security Considerations

Include any relevant security considerations or best practices, especially if the tool involves handling sensitive data.
## Error Handling

If you encounter issues, refer to the troubleshooting section and ensure dependencies are correctly installed.

## Deployment Options

Consider different deployment options, such as deploying on a cloud platform or integrating with an existing system.

## Acknowledgments

We acknowledge the contributions of third-party tools and libraries used in this project.

## Security Considerations

Include any relevant security considerations or best practices, especially if the tool involves handling sensitive data.

## User Guide

1. Enter a search query in the provided input field.
2. Click the "Submit" button to trigger the recommendation generation.
3. View the recommended offers and their similarity scores in the output section.

Feel free to explore and adapt the tool based on your evolving requirements. Collaboration is welcomed to refine and expand the tool further.
