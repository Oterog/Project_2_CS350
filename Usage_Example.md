# Usage Example

## Table of Contents

- [Steps](#steps)

    - [Step 1](#step-1---install-required-libraries-in-bash)

    - [Step 2](#step-2---define-your-data-model-in-json)

    - [Step 3](#step-3---configure-gora-properties-in-properties)

    - [step 4](#step-4---write-the-code-in-python)

- [Explanation of Steps](#explanation-of-steps)

## Steps

### Step 1 - Install Required Libraries in .bash

- First, ensure you have Apache Gora and its dependencies installed.

```bash
{
    pip install pygora
}
```

### Step 2 - Define Your Data Model in .json

- Secondly, create an Avro schema for your data. The example here is for a webpage

```Json
{
    "type": "record",
    "name": "WebPage",
    "namespace": "example.gora",
    "fields": 
    [ 
        {"name": "url", "type": "string"}, 
        {"name": "content", "type": "string"}, 
        {"name": "parsedContent", "type": "string"}, 
        {"name": "outlinks", "type": {"type": "array", "items": "string"}}, 
        {"name": "headers", "type": {"type": "map", "values": "string"}} 
    ]
}
```

### Step 3 - Configure Gora Properties in .properties

- Update your gora.properties to specify your datastore.

```properties
{
    gora.datastore.default=org.apache.gora.hbase.store.HBaseStore
    gora.datastore.autoCreateSchema=true
}
```

### Step 4 - Write the Code in .Python

- Here’s a simple Python script to interact with the Gora data model.

```python
{
    from pygora.client import GoraClient
    from pygora.models import Record

# Initialize the Gora client
    client = GoraClient(schema_file='path/to/webpage.avsc', store='org.apache.gora.hbase.store.HBaseStore')

# Create a new record
    webpage = Record
    (
        url='https://example.com',
        content='<html>...</html>',
        parsedContent='Example Content',
        outlinks=['https://example1.com', 'https://example2.com'],
        headers={'Content-Type': 'text/html'}
    )

# Persist the record
    client.put(webpage.url, webpage)

# Retrieve the record
    retrieved_webpage = client.get('https://example.com')
    print(f'Retrieved WebPage: {retrieved_webpage}')

# Close the client connection
    client.close()

}
```

## Explanation of Steps

- Initialization: The GoraClient is initialized with the schema file and the specified datastore.

- Record Creation: A Record object is created and populated with data.

- Persistence: The put method is used to store the record in the database.

- Retrieval: The get method fetches the record from the database, and the result is printed.

- Close Connection: Finally, the client connection is closed properly.

This script demonstrates how to define a data model, store data, and retrieve it using Apache Gora with Python.
