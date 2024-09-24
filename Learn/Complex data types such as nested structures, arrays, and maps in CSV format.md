When dealing with complex data types such as nested structures, arrays and maps in CSV format, handling them can be more challenging than in Parquet because CSV files are inherently flat and do not support hierarchical or complex data structures natively.

Here's how to approach handling complex data types like nested structures, arrays, and maps in CSV, including how to preprocess or transform them into a more usable format for Pandas, ETL, pipelines, or loading into databases like Redshift.

## Nested Structures (Structs)
Since CSV is a flat format, nested structures cannot be directly represented. Instead, nested fields must either be flattened into separate columns or stored as a serialised format (e.g., JSON strings).
### Example (Nested Structure):
Suppose you have a nested JSON-like structure:
```JSON
{
	"user_id" : 1,
	"user_info": {
		"name" : "Alice",
		"age" : 30,
		"address" : {
			"city" : "New York",
			"zip" : 10001
		}
	}
}
```
In CSV, you could flatten this structure like so:

| user_id | user_info_name | user_info_age | user_info_address_city | user_info_address_zip |
| ------- | -------------- | ------------- | ---------------------- | --------------------- |
| 1       | Alice          | 30            | New York               | 10001                 |

### Solution in Pandas:

You need to flatten these nested structures manually or via a script that flattens in data before writing to CSV.
```python
import pandas as pd
# Sample CSV where nested fields are represented as serialized JSON
df = pd.read_csv('data.csv')
# Flatten the fields
df['user_info_name'] = df['user_info'].apply(lambda x: x['name'])
df['user_info_age'] = df['user_info'].apply(lambda x: x['age'])
df['user_info_address_city'] = df['user_info'].apply(lambda x: x['address']['city'])
df['user_info_address_zip'] = df['user_info'].apply(lambda x: x['address']['zip'])
# Drop original nested column
df = df.drop('user_info',axis=1)
```

## Arrays
In CSV, arrays (like lists) are usually stored as strings, separated by some delimiter (e.g., commas, semicolons). This poses a challenge when trying to process them, as they need to be split back into individual elements.
### Example (Array):
```json
{
	"user_id": 1,
	"user_purchases": [100, 200, 300]
}
```
In CSV, this might be represented as:

| user_id | user_purchases |
| ------- | -------------- |
| 1       | 100,200,300    |
### Solution in Pandas:
You can **split** the array-like fields back into Python lists and further process them (e.g., by exploding them into multiple rows or multiple columns).
```python
# Read CSV where arrays are stored as comma-seperated strings
df = pd.read_csv('data.csv')

# Split the string back into a list
df['user_purchases'] = df['user_purchases'].apply(lambda x: x.split(','))

# Option 1: Explode the array into multiple rows
df_exploded = df.explode('user_purchases')

# Option 2: Split into seperate columns
df[['purchase1','purchase2','purchase3']] = pd.DataFrame(df['user_purchases'].tolist(),index=df)
```

## Maps (Dictionaries)
In CSV, maps (key-value pairs) are often represented as strings in some serialised format, like JSON. You need to **deserialise** them to work with them properly in Pandas.
### Example (Map):
```json
{
	"user_id": 1,
	"user_preferences": {
		"theme": "dark",
		"notifications": "enabled"
	}
}
```
In CSV, this might be represented as:

| user_id | user_preferences                            |
| ------- | ------------------------------------------- |
| 1       | {"theme":"dark", "notifications":"enabled"} |
### Solution in Pandas:
You need to parse the JSON-like string back into a dictionary and then flatten it.
```python
import json

# Read CSV where maps are stored as JSON strings
df = pd.read_csv('data.csv')

# Convert the JSON-like string back to a dictionary
df['user_preferences'] = df['user_preferences'].apply(lambda x: x['notifications'])

# Drop the original map column if needed
df = df.drop('user_preferences', axis=1)
```
