# Main purposes and characteristics

## Table of contents

- [Main Purposes](#main-purposes)

    - [Data Storage Abstraction](#data-storage-abstraction)
    
    - [Data Analysis](#data-analysis)

    - [In-Memory Computation](#in-memory-computation)

    - [Flexibility and Extensibility](#flexibility-and-extensibility)

    - [Schema Management](#schema-management)

- [Key Characteristics](#key-characteristics)

    - [Pluggable Backends](#pluggable-backends)

    - [Object-to-Store Mapping](#object-to-store-mapping)

    - [Big Data Integration](#big-data-integration)

    - [Schema Evolution](#schema-evolution)

    - [Efficient Data Querying](#efficient-data-querying)

    - [Language Support](#language-support)

    - [Community-Driven and Open Source](#community-driven-and-open-source)

## Main Purposes

### Data Storage Abstraction

- Simplifies the interaction with various NoSQL databases and storage backends.

- Supports heterogeneous data models (columnar, document-oriented, key-value, etc.).

### Data Analysis

- Provides tools to analyze large-scale data efficiently.

- Integrates with big data processing frameworks like Apache Hadoop and Apache Spark for scalable analysis.

### In-Memory Computation

- Optimized for handling large datasets in-memory for high-performance applications.

### Flexibility and Extensibility

- Allows developers to work seamlessly with multiple data stores without locking into a single backend technology.

### Schema Management

- Automatically maps structured data schemas into Java objects, simplifying development

## Key Characteristics

### Pluggable Backends

- Supports multiple data stores, including HBase, Cassandra, MongoDB, DynamoDB, Accumulo, and more.

- Extensible to support new data stores as required.

### Object-to-Store Mapping

- Uses a data mapping model similar to ORM (Object-Relational Mapping) for NoSQL.

- Handles schema definition and data persistence with minimal boilerplate.

### Big Data Integration

- Provides seamless integration with distributed computing platforms.

- Allows users to write MapReduce jobs for analyzing data stored in Gora-supported backends.

### Schema Evolution

- Supports Avro serialization for schema evolution, enabling forward and backward compatibility.

### Efficient Data Querying

- Offers APIs for efficient querying, pagination, and data retrieval.

### Language Support

- Primarily designed for Java developers, with a focus on providing easy-to-use APIs.

### Community-Driven and Open Source

- Maintained as an Apache Software Foundation project with regular updates and community contributions.