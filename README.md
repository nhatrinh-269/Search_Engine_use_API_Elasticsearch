# Build Simple Search Engine with API Elasticsearch

## Description
Search engines provide users with quick and easy access to information. By simply entering a few keywords, users can find information on virtually any topic on the Internet within seconds. Developing a personalized search tool helps businesses and organizations easily search and analyze data within their own databases. This project creates a simple search tool using the Elasticsearch API, with the dataset being a copy of emails retrieved from Google Takeout.

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
1. Read the `.mbox` file and extract necessary information such as subject, sender, receiver, date, email content and data cleaning
2. Use PySpark to create a DataFrame from the extracted email data and normalize the data. 
4. Store the processed information in a MySQL database.

### Step 2: Index Data into Elasticsearch
1. Connect to MySQL and retrieve data from the stored tables.
2. Use the Elasticsearch API to index the data from MySQL into Elasticsearch.
3. Ensure each email, sender, and receiver is accurately indexed with related information.

### Step 3: Search in Elasticsearch
1. Create a search tool using the Elasticsearch API.
2. Perform searches on fields such as email subject, email content, sender, and receiver.
3. Display the search results, including detailed information of the found emails.

### Setting Up Elasticsearch and Obtaining API Credentials
1. **Download and Install Elasticsearch**:
   - Download Elasticsearch from the [official website](https://www.elastic.co/downloads/elasticsearch).
   - Follow the installation instructions for your operating system.

2. **Run Elasticsearch**:
   - Start the Elasticsearch service. This can usually be done by running the `elasticsearch` executable from the installation directory.

3. **Set Up Elasticsearch Cloud (Optional)**:
   - Sign up for an Elasticsearch Cloud account at [Elastic Cloud](https://cloud.elastic.co/).
   - Create a new deployment and take note of the `Cloud ID`, `username`, and `password`.

4. **Obtain API Credentials**:
   - If you are using Elasticsearch locally, you typically do not need special API credentials.
   - For Elastic Cloud, use the `Cloud ID` and the credentials provided during the setup.

5. **Connect to Elasticsearch**:
   - Use the `elasticsearch` Python library to connect to your Elasticsearch instance or deployment.
   - Example connection code:
     ```python
     from elasticsearch import Elasticsearch

     # For local Elasticsearch
     es = Elasticsearch()

     # For Elastic Cloud
     cloud_id = "Your_Cloud_ID"
     username = "Your_Username"
     password = "Your_Password"
     es = Elasticsearch(cloud_id=cloud_id, basic_auth=(username, password))
     ```

### Obtaining `Unread.mbox` from Google Takeout
1. Go to [Google Takeout](https://takeout.google.com/).
2. Select "Mail" to include in your archive.
3. Choose the desired export options and create the export.
4. Once the export is complete, download the archive and extract it to find the `Unread.mbox` file in the `Mail` folder.

## Contribution
If you want to contribute to this project, please create a pull request or open an issue on GitHub.

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
