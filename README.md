Here's the README file translated into English, formatted for a GitHub repository:

---

# Email Processing and Search Engine Project

## Description
This project processes emails from an `.mbox` file, extracts information, and stores it in a MySQL database using PySpark for processing and normalization. The project then uses the Elasticsearch API to index the data and provide a powerful search engine.

## Installation

### System Requirements
- Python 3.x
- Apache Spark
- MySQL
- Elasticsearch

### Required Python Libraries
Install the necessary Python libraries:
```bash
pip install pyspark
pip install mysql-connector-python
pip install elasticsearch
```

## Usage

### Step 1: Process Emails and Store in MySQL
1. Read the `.mbox` file and extract necessary information such as subject, sender, receiver, date, and email content.
2. Use PySpark to create a DataFrame from the extracted email data.
3. Normalize the data and remove unwanted escape characters.
4. Store the processed information in a MySQL database.

### Step 2: Index Data into Elasticsearch
1. Connect to MySQL and retrieve data from the stored tables.
2. Use the Elasticsearch API to index the data from MySQL into Elasticsearch.
3. Ensure each email, sender, and receiver is accurately indexed with related information.

### Step 3: Search in Elasticsearch
1. Create a search tool using the Elasticsearch API.
2. Perform searches on fields such as email subject, email content, sender, and receiver.
3. Display the search results, including detailed information of the found emails.

## Contribution
If you want to contribute to this project, please create a pull request or open an issue on GitHub.

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

This README provides an overview of the main steps in your project without delving into code specifics, suitable for a GitHub repository.
