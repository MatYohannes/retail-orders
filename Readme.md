# Data Engineering Project

## Overview
This project utilizes the Kaggle API to download a dataset, processes the data using pandas in a Jupyter Notebook, and uploads the cleaned data to AWS RDS. SQL queries are performed on the RDS instance, and the results are exported as CSV files. Finally, the data is visualized using Tableau Public to create an interactive dashboard.

## Table of Contents
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Scripts](#scripts)
- [Data](#data)
- [Dashboard Screenshot](images/dashboard.png)
- [Contributing](#contributing)
- [License](#license)

## Technologies Used
- Python
- Jupyter Notebook
- pandas
- AWS RDS
- AWS Secrets Manager
- Tableau Public
- Kaggle API

## Project Structure
/YourProjectDirectory
│
├── Build-files
│   ├── deploy-vpc         # Shell script to deploy VPC using vpc-template.yaml
│   ├── deploy-rds         # Shell script to deploy RDS using rds-template.yaml
│   ├── create-secret       # Shell script to create an AWS Secret Key
│   ├── delete-secret       # Shell script to delete AWS Secret Key
│   └── cleanup             # Shell script to delete VPC and RDS stacks
│
├── Data
│   ├── dataset.zip         # Original dataset downloaded from Kaggle
│   ├── cleaned_data.csv    # CSV file of cleaned data
│   ├── query_results_1.csv  # CSV file of SQL queried dataframe 1
│   ├── query_results_2.csv  # CSV file of SQL queried dataframe 2
│   ├── query_results_3.csv  # CSV file of SQL queried dataframe 3
│   ├── query_results_4.csv  # CSV file of SQL queried dataframe 4
│   └── query_results_5.csv  # CSV file of SQL queried dataframe 5
│
└── data_processing.ipynb   # Jupyter Notebook with data processing work

## Setup Instructions
1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd YourProjectDirectory
2. Install necessary packages: Make sure you have the required Python packages installed.
    pip install -r requirements.txt
3. Configure AWS CLI: Ensure that your AWS CLI is configured with the appropriate access and secret keys.
4. Run the scripts in Build-files:
- Deploy the VPC:
  - ./Build-files/deploy-vpc
- Deploy the RDS instance:
  - ./Build-files/deploy-rds
- Create a secret for database credentials:
  - ./Build-files/create-secret

## Usage
1. Data Processing: Open the Jupyter Notebook (data_processing.ipynb) and follow the steps to process the data, upload it to AWS RDS, and run SQL queries.
2. Export Data: After processing, export your dataframes as CSV files for visualization.
3. Visualize with Tableau: Upload the CSV files to Tableau Public to create your dashboard.

## Scripts
- deploy-vpc: Deploys a Virtual Private Cloud using the specified CloudFormation template.
- deploy-rds: Deploys an RDS instance with specified configurations.
- create-secret: Creates an AWS Secret Key to manage database credentials securely.
- delete-secret: Deletes the AWS Secret Key when no longer needed.
- cleanup: Removes both the VPC and RDS stacks to free up resources.

## Data
The Data folder contains:

    The original dataset from Kaggle in a ZIP file.
    The cleaned data CSV file.
    CSV files containing the results from SQL queries executed on the RDS instance.

## Dashboard Screenshot

[View my Tableau Dashboard](https://public.tableau.com/app/profile/mathewos.yohannes/viz/Retail-Orders/Dashboard1?publish=yes)
![Retail Orders Dashboard](screenshots/dashboard.png)

## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue for any improvements or suggestions.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

### Additional Information Needed
1. The repository URL to include in the setup instructions.
2. Any specific requirements you have (like a `requirements.txt` file) that should be included in the setup instructions.
3. Any particular license you want to mention.
4. Additional details you want to include in any of the sections.

Feel free to modify or expand any sections based on your project specifics!
