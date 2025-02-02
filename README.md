# TOPSIS for Pre-Trained Models on Text Conversational AI

This project applies the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method on pre-trained conversational models. The process involves generating initial parameters, applying TOPSIS to rank models, and generating both output data and performance graphs.

## Workflow:
1. **gen_values.ipynb**:
   - Generates the initial parameters.
   - Saves them to a CSV file named `initial_data.csv`.
  
2. **TOPSIS Application**:
   - Uses the custom Python library `topsis-arnav-102203979` to apply the TOPSIS method on the data.
   - Produces an output CSV file with the ranked models.

3. **Graphs**:
   - The results are visualized in **images.png**, which shows the model ranking and other related information.

## Table of Results:
Here is a sample table of pre-trained conversational models and their respective metrics:

| Model Name                         | Score | Metric 1 | Metric 2 |
|-------------------------------------|-------|----------|----------|
| facebook/blenderbot-400M-distill   | 0.72  | 25.4     | 1.12     |
| microsoft/DialoGPT-medium          | 0.68  | 23.8     | 0.95     |
| t5-small                            | 0.74  | 26.1     | 0.85     |
| EleutherAI/gpt-neo-1.3B            | 0.81  | 28.9     | 1.75     |
| HuggingFaceH4/zephyr-7b            | 0.85  | 30.2     | 2.1      |

## How to Use:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/topsis-pretrained-models.git
2. Run the gen_values.ipynb notebook to generate initial data.
3. Apply TOPSIS through the library:
   ```bash
   import topsis_arnav_102203979
   topsis 'Initial_Data.csv' '1,1,1' '+,+,-' 'output.csv'
4. View the output.csv and images.png for the results.
![TOPSIS Results Graph](images.png)
