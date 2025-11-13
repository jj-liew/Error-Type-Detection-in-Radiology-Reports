# Error Type Detection in Radiology Reports using Hugging Face Transformers
This project utilizes the ReXerr-v1 dataset to automatically categorize error types in radiology reports. The objective of this experiment is to explore the performance of various transformer models, including an ensemble approach that combines the strengths of two different models. This project includes data preprocessing, fine-tuning and evaluation steps of these models.

## Corpus 
The ReXerr-v1 report-level dataset is used to conduct all experiments in this study. Each row consists of an original radiology report and a version with errors injected. The plausibility of the generated errors is validated through clinical feedback. Out of 100 randomly sampled report pairs (original and erroneous), only 17 were deemed not realistically plausible. The error categories include: 'Add contradiction', 'Add medical device', 'Add repetitions', 'Add typo', 'Change location', 'Change measurement', 'Change name of device', 'Change position of device', 'Change severity', 'Change to homophone', 'False negation', and 'False prediction'. Each error-injected report is generated using GPT-4, containing 3 of the error categories listed above. These categories are carefully synthesized with the help of three board-certified radiologists to ensure authenticity.

The dataset and related article can be found here: [https://physionet.org/content/rexerr-v1/1.0.0/](https://physionet.org/content/rexerr-v1/1.0.0/).

## Reproducing the results
To run the notebook, the three ReXErr-report-level csv files has to be downloaded and stored in your directory. Follow along the notebook to reproduce the results.

## Conclusion
This project uses only 10% of the training dataset due to the limitation of computational time and power. However, the existing pretrained transformer models generally perform well for downstream tasks, without needing too many resources. The approaches demonstrated in this project can be a viable way to perform specific downstream tasks when resources are limited.
