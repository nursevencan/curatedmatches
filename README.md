# curatedmatches

**Customer Similarity and Matching Script**

This script performs customer similarity analysis and generates customer matches based on vector embeddings calculated from customer attributes. It uses the SpaCy library for natural language processing and calculates cosine similarity to identify similar customers.

**Prerequisites**
- Python 3.x
- Required Python packages: pandas, numpy, json, spacy, scipy
- You'll need to have the SpaCy model "en_core_web_md" installed. If not already installed, run the following command:

python -m spacy download en_core_web_md

**Usage**
Clone or download this repository to your local machine.

**Install the required Python packages if you haven't already:**
pip install pandas numpy spacy scipy
Install the SpaCy model "en_core_web_md":
python -m spacy download en_core_web_md

Modify the customer_data.csv file: 
Replace it with your own customer data in CSV format. Ensure that the CSV file contains the specified attributes for vector embeddings: 'Name', 'ID', 'Fellowships', 'City', 'Country', 'Bio', 'Company', 'Role', 'Success', 'Interest'.

**Run the Script**
The script will generate a matches.json file containing the top matches for each customer based on cosine similarity of vector embeddings.

**Script Workflow**
Load necessary Python libraries.
Load the SpaCy model "en_core_web_md".
Load customer data from customer_data.csv.
Calculate vector embeddings for each customer using their attributes.
Calculate cosine similarity matrix between all pairs of customers.
Select the k-nearest neighbors for each customer (k specified in the script) and recommend top matches.
Save the generated matches to a JSON file.

**Notes**
The script assumes that you have a CSV file named customer_data.csv with the specified attributes. Ensure that the CSV file is correctly formatted.
The vector embeddings are calculated based on the concatenated attributes of each customer.
Modify the k variable in the script to adjust the number of nearest neighbors to consider for matching.

**Disclaimer**
This script is provided as a tool for performing customer similarity analysis and generating matches based on provided attributes. The accuracy of matches depends on the quality and relevance of the customer data and attributes.
