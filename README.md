# CSV-to-JSON-Converter.-python

import csv
import json

# CSV file ko read karna
with open("input.csv", "r") as csv_file:
    csv_reader = csv.DictReader(csv_file)
    data = list(csv_reader)

# Data ko JSON file mein write karna
with open("output.json", "w") as json_file:
    json.dump(data, json_file, indent=4)

print("CSV data successfully converted to JSON!")
print("JSON file created: output.json")
