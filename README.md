# Al-Tadmuriyah Text Modeling Project
Fine-tuning the AraGPT2-large model on Al-Tadmuriyah by Shaykh al-Islam Ibn Taymiyyah. The project preserves the unique language of the text and explores future fine-tuning for tasks like question-answer generation and summarization to enhance engagement with classical Islamic scholarship.


---



## Overview

This project focuses on fine-tuning the AraGPT2-large model on classical Islamic texts, particularly Al-Tadmuriyah by Shaykh al-Islam Ibn Taymiyyah. The objective is to train a language model to generate text that mirrors the unique linguistic style and content of Al-Tadmuriyah. This project is part of a larger initiative to preserve the works of influential scholars by applying advanced natural language processing (NLP) techniques. The project consists of several phases, including data extraction, model fine-tuning, hyperparameter optimization, and evaluation.

## Project Components

### 1. Data Extraction

Description: The Al-Tadmuriyah text was scraped and extracted from HTML files obtained from the Al-Shamela library. The HTML files contain inconsistencies such as headers, page numbers, and formatting issues, which were cleaned using Python libraries like Beautiful Soup.

Goal: Extract, clean, and prepare the text for training the language model.

Output: Cleaned dataset saved in CSV format and uploaded to Hugging Face datasets for public access.


### 2. Baseline Model & Hyperparameter Optimization

Description: The AraGPT2-large model was initially trained on the cleaned Al-Tadmuriyah text. However, the baseline model performed poorly, prompting a grid search over several hyperparameters to identify the best configuration for this specific task.

Goal: Fine-tune the AraGPT2-large model to accurately represent the text of Al-Tadmuriyah.

Output: Logs, visualizations, and hyperparameter configurations, as well as the fine-tuned model uploaded to Hugging Face Hub.


### 3. Data Visualization

Description: This notebook visualizes the results from the grid search and analyzes how different hyperparameters influenced the model’s performance. TensorBoard was used to log and monitor training progress.

Goal: Identify the best hyperparameters and analyze their effect on model performance.

Output: Graphs and insights from the grid search.


### 4. Building the Final Model

Description: The best combination of hyperparameters identified from the grid search was used to build the final model. This model was then fine-tuned specifically on Al-Tadmuriyah text and uploaded to Hugging Face Hub for public use.

Goal: Fine-tune the final model with optimal hyperparameters for Al-Tadmuriyah text generation.

Output: Final fine-tuned model uploaded to Hugging Face Hub.


### 5. Model Testing

Description: In this phase, the final Al-Tadmuriyah model was loaded and tested for performance. The focus was on generating text in the style of Shaykh al-Islam Ibn Taymiyyah and evaluating the model’s output quality.

Goal: Assess the performance and output quality of the fine-tuned model.

Output: Test results and observations on the model’s strengths and limitations.


## Project Structure

├── data/
│   └── Al-Tadmuriyah_cleaned.csv  # Cleaned dataset
├── al_tadmreyyah_model
│   ├── 1_al_tadmoreyyah.ipynb    # Extract and clean the text
│   ├── 2_al_tadmoreyyah_model.ipynb     # Build baseline model and perform grid search
│   ├── 3_vis_result.ipynb # Visualize grid search results
├── final_model_build.ipynb  # Build and fine-tune final model
│   └── 1_test_model.ipynb      # Test the final model
│   └── 2_ logs (10).zip  # logs for the final model
│   └── 3_training_public_al_tadmoreyyah_model.ipynb # train the final model
└── README.md              # This file

## Getting Started

### Prerequisites

To run this project, you will need the following libraries:

Python 3.8+

Hugging Face Transformers

TensorFlow / PyTorch (depending on your setup)

Pandas

Beautiful Soup (for HTML parsing)

Hugging Face Datasets

TensorBoard (for visualization)



Clone this repository:

git clone https://github.com/yourusername/Al-Tadmuriyah-Modeling.git
cd Al-Tadmuriyah-Modeling


## Running the Notebooks

1. Data Extraction: Open and run the 1_data_extraction.ipynb notebook to extract and clean the text from the HTML files.


2. Baseline Model & Grid Search: Open 2_baseline_model.ipynb to train the baseline AraGPT2 model and perform a grid search for the best hyperparameters.


3. Data Visualization: Use 3_data_visualization.ipynb to visualize the results from the grid search.


4. Final Model Building: In 4_final_model_build.ipynb, apply the best hyperparameters and fine-tune the final model on the Al-Tadmuriyah dataset.


5. Model Testing: Use 5_model_testing.ipynb to load and evaluate the final model’s performance.



## Results

The final model trained on the text of Al-Tadmuriyah is available on Hugging Face Hub. It generates coherent and contextually relevant text that aligns with the style of Shaykh al-Islam Ibn Taymiyyah.

Link to the model on Hugging Face: Al-Tadmuriyah Model

## Future Work

Insha'Allah, the next phase of this project will focus on further fine-tuning the Al-Tadmuriyah model to improve its utility in several key areas. Specifically, I plan to:

Fine-tune the model to generate questions and answers based on the text, aligning with the format and style found in Shaykh al-Islam Ibn Taymiyyah's works.

Adapt the model for text summarization, making it easier to distill key insights and arguments from Al-Tadmuriyah into concise summaries.

Enhance the model’s ability to assist in scholarly analysis by providing more accurate and contextually aware responses in the style of Shaykh al-Islam Ibn Taymiyyah.


These fine-tuning tasks will allow the model to become a more valuable resource for those studying and engaging with the works of Shaykh al-Islam Ibn Taymiyyah, especially within the context of his Al-Tadmuriyah writings.


## Contributing

Contributions are welcome! If you have any ideas or suggestions, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact

For any inquiries or feedback, please contact me at [ahmadalraab2@gmail.com].
