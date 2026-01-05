## Week 5: Integration

This week is about connecting the Python environment to the Ethereum blockchain. We will use `web3.py` to make our Python script "talk" to the smart contract.

### 1. The API / Backend Logic
You don't necessarily need a full web server, but organizing your code as an API allows a frontend to easily talk to it later.

* **Framework:** Use FastAPI or Flask(you can use any framework just make sure there is a corresponding contract calling library in that language like web3.py in python). FastAPI is generally preferred for ML projects because it's faster and handles data types better.
* **Workflow:**
    1. Receive transaction data.
    2. Run ML model -> Get Prediction.
    3. Hash the data -> Get SHA-256 Hash.
    4. Trigger the blockchain transaction.

**Resources:**
* [FastAPI Tutorial (User Guide)](https://fastapi.tiangolo.com/tutorial/)

### 2. Web3.py Integration
This is the bridge. Your Python script needs to sign transactions and send them to the network.

**Key Concepts to Implement:**
* **Provider:** This is how you connect to the network. You will likely use a local node (like Ganache) or a remote node (via Infura/Alchemy if using a testnet).
* **ABI (Application Binary Interface):** When you compile your contract in Remix, you get a JSON list called the ABI. Python needs this to know what functions are available in your contract.
* **Signer:** You need a private key to pay for gas. Never hardcode real private keys. Use environment variables or test accounts.

**Resources:**
* [Web3.py Documentation - Quickstart](https://web3py.readthedocs.io/en/stable/quickstart.html)
* [Interacting with Contracts using Web3.py](https://web3py.readthedocs.io/en/stable/contracts.html)

### 3. Frontend (Optional)
If you finish early, create a simple interface where a user can paste a transaction hash and see the result.

* **Tools:** Streamlit is the easiest option for Python developers. It allows you to build a UI entirely in Python without writing HTML/CSS.
* **Resource:** [Streamlit Documentation](https://docs.streamlit.io/)
