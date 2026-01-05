## Context
We are building a system that bridges Machine Learning with Blockchain to create an immutable record of financial fraud. The workflow is straightforward: raw transaction data is processed by a Python-based ML model to predict if it is fraudulent. To ensure data privacy and integrity, we hash the transaction data (using SHA-256) and store only the hash and the prediction result on the Ethereum blockchain. This prevents anyone from tampering with the history of fraud detection.

The next two weeks are focused on building the individual components (Week 4) and then wiring them together (Week 5).

---

## Week 4: Component Construction

This week is about building the three core pillars of the project in isolation: the Classifier, the Hashing logic, and the Smart Contract.

### 1. The Machine Learning Classifier
You need to build a binary classifier (Fraud vs. Legit).You can use any algorithm which gives you the best result.


### 2. SHA-256 Hashing
Before we touch the blockchain, we need a way to fingerprint our data. We will use the SHA-256 algorithm.

* **Concept:** It takes an input of any size and produces a fixed-size string (the hash). A slight change in input results in a completely different hash.
* **Implementation:** Use the built-in `hashlib` library in Python.
* **Resource:** [Python hashlib documentation](https://docs.python.org/3/library/hashlib.html)

### 3. Smart Contract Development
You need to write a Solidity contract that acts as the storage layer. Do not worry about connecting it to Python yet; just write and test it in Remix.

**Required Solidity Syntax & Concepts:**
To complete the assignment, you will need to understand specific syntax elements. Use the [Solidity Docs](https://docs.soliditylang.org/) as your primary reference.

* **Structs:** You need a way to group data. Look up how to define a `struct` to hold multiple variables (like the hash, the prediction result, and a timestamp) under one name.
* **Mappings:** This is your database. Look up the syntax for `mapping(Type => Type)`. You will likely need to map a `bytes32` (the hash) or `string` to your struct.
* **Functions:**
    * **State-Changing Functions:** Functions that write data cost gas. You will need one to add a new record.
    * **View Functions:** Functions that only read data are free. You need one to retrieve the status of a hash.
* **Events:** To make the frontend/logs readable, look up how to `emit` an event whenever a new record is added.

Its just a example skelton how your contract should look like you can choose any other implementation also as far as it works.
