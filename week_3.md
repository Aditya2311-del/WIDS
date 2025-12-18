# 🌐 Week 3: Blockchain Learning

This week’s plan is designed to take you from the **first principles of blockchain** to **writing and deploying your first smart contracts**.

---

## 💡 Why store data (such as ML predictions) on a blockchain?

Since you have already built (or will build next week) a model to predict fraud, you might wonder why we wouldn’t simply use a traditional database. Here’s why blockchain makes sense in certain cases:

- **Immutability:** Once a prediction is stored on-chain, it cannot be edited or deleted by anyone—not even an administrator. This creates a permanent, tamper-proof record of every prediction your model makes.
- **Decentralized Verification:** Instead of trusting a private server, anyone can independently verify the “Legit/Fraud” status of a transaction using the public ledger.
- **Censorship Resistance:** No single authority can shut down the blockchain or selectively hide records.

---

## 📚 Core Resources

- **Conceptual Guide:**  
  TutorialsPoint Blockchain Series  
  https://www.tutorialspoint.com/blockchain/index.htm

- **Must-Watch:**  
  3Blue1Brown — *How Bitcoin Works*  
  https://youtu.be/bBC-nXj3Ng4

- **Deep Dive (Optional):**  
  *Blockchain from First Principles* (Lectures 1–9)  
  https://youtube.com/playlist?list=PLfmqK5mMBWj9dEmo91RBJd3xHx4TQi8bA  
  > Not required for this project, but useful if you want to understand how Bitcoin works internally.

- **Reference (Optional):**  
  Bitcoin Whitepaper  
  https://bitcoin.org/en/bitcoin-paper

- **Coding Resource:**  
  Solidity 0.8 Playlist  
  https://www.youtube.com/playlist?list=PLO5VPQH6OWdVQwpQfw9rZ67O6Pjfo6q-p

---

## 📅 7-Day Learning Plan

### Day 1 & 2: Understanding the Ledger

- **Watch:**  
  *But how does Bitcoin actually work?* (3Blue1Brown)

- **Read:**  
  TutorialsPoint Blockchain Series  
  This may feel overwhelming, so **only the following topics are required for this project**:
  - Blockchain — Introduction  
  - History of Blockchain  
  - Blockchain Technology (high-level understanding only)  
  - Blockchain and Cryptography  
  - Smart Contracts  
  - Briefly review the Ethereum section as well

- **Focus:**  
  Pay close attention to **SHA-256 hashing**. This “digital fingerprint” concept will be used next week.

---

### Day 3: Bitcoin Architecture

- **Watch:**  
  *Blockchain from First Principles* (Lectures 1–9)

- **Goal:**  
  Understand how Bitcoin works from first principles.  
  **This is not required for the project**, but it will deepen your understanding.

- **Optional Reading:**  
  Bitcoin Whitepaper

---

### Day 4: Environment Setup

- **Task 1: Install MetaMask**  
  Required only if you plan to work locally instead of using Remix.  
  Visit https://metamask.io, install the extension, and create a wallet.  
  **Store your Secret Recovery Phrase securely offline.**

- **Task 2: Remix IDE**  
  Open https://remix.ethereum.org.  
  This will be your online Solidity code editor.

- **Task 3: Git Integration in Remix**  
  Watch: *Git in Remix Tutorial*  
  https://youtu.be/LNKv3ysoVeE  
  Learn how to connect Remix directly to your GitHub repository.

---

### Day 5: Solidity 101 (Basics)

- **Resource:**  
  Solidity 0.8 Playlist

- **Watch and code along:**
  1. Hello World  
  2. Value Types (`uint`, `int`, `bool`)  
  3. State Variables vs Local Variables  
  4. Functions (`view`, `pure`, and simple returns)

---

### Day 6: Data Structures in Solidity

- **Watch and code along:**
  1. Arrays (fixed and dynamic)  
  2. **Mappings** (most important for storing data)  
  3. Structs (custom data types)  
  4. Constructors

---

### Day 7: Final Learning Assignment

- **Goal:**  
  Build a **Digital Notebook** smart contract.

- **Task:**  
  Write a contract that allows users to store and retrieve messages linked to their wallet address.

- **Submission:**  
  Push your code to your GitHub repository (the one shared in the Week 1 Google Form) using the Remix Git plugin.

---

## 🚀 Learning Assignment: `DigitalNotebook.sol`

Create a smart contract that acts as a simple personal storage system.

### Requirements

1. **Struct:**  
   Define a `Note` struct containing:
   - `string message`
   - `uint timestamp`

2. **Mapping:**  
   Create a mapping that links a user’s `address` to an array of `Note` structs.

3. **Function: `addNote`**
   - Takes a `string` as input  
   - Stores the message and the current time (`block.timestamp`)  
   - Associates the note with `msg.sender`

4. **Function: `getNotes`**
   - Allows a user to retrieve all of their stored notes

5. **Bonus:**  
   Add a global counter that tracks the total number of notes created by all users.

---

## 📤 How to Submit

1. Write the contract in **Remix IDE**  
2. Compile it using the **Solidity Compiler** tab  
3. Use the **Git Plugin** in Remix to commit and push the `.sol` file  
4. **Important:** Push the code to the same repository shared in the Week 1 form. No new form is required.

Note:This is a very basic assignment, so if you have some experience working with blockchains then you can create a more complex contracts like a bridging contract or a staking contract(not reccomended if studying for the first time)
