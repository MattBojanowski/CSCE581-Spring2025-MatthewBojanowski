# AI Testcase (TC) Template
_ // This file has a template for recording testcases for chatbots_

### 1. TC-identifier: TC-FD-001
_ // Identifier for the test case: Unique ID for the financial fraud detector test case._

### 2. TC-name: High Amount Transfer Fraud Detection
_ // Name for the test case: Testing detection of fraud in a high-value transfer transaction._

### 3. TC-objective: 
_ // Describe what we are trying to evaluate from the test case: Evaluate the AI model's ability to correctly identify fraudulent transactions based on transaction features such as amount, balances, and transaction type. Specifically, test if the model flags a suspicious high-amount transfer as fraud._

### 4. TC-input: 
_ // The input to be given: A dictionary representing a single transaction with the following data:
{
    'step': 1,
    'type': 'TRANSFER',
    'amount': 1000000.0,
    'nameOrig': 'C123456789',
    'oldbalanceOrg': 1000000.0,
    'newbalanceOrig': 0.0,
    'nameDest': 'C987654321',
    'oldbalanceDest': 0.0,
    'newbalanceDest': 1000000.0,
    'isFlaggedFraud': 0
}
This simulates a large transfer where the originator's balance goes to zero and the destination receives the full amount, which could indicate fraud._

### 5. TC-reference-output: 
_ // The output to be used as reference to compare and evaluate AI: The model should predict 1 (fraud detected). Expected output message: "Financial fraud is detected."_

### 6. TC-harm-risk-info: 
_ // Risk information that the test case may be associated with. Also mention harm categories from the book: HC1-incorrect-info, HC2-opinion-manipulation, HC3-unstable-extrauserinfo, HC4-incomprehensible-ai. Or, use HC5 for others. HC5 - Potential financial harm if the model fails to detect fraud, leading to monetary loss for users or institutions. Incorrect classification could result in false negatives (missing fraud) or false positives (blocking legitimate transactions)._

### 7. TC-other-info: 
_ // Any other information to be recorded: This test case uses synthetic data similar to the training dataset. For comprehensive testing, additional test cases should cover non-fraudulent transactions, edge cases like zero amounts, and various transaction types (CASH_OUT, PAYMENT, etc.). Ensure the model is loaded from '../code/custom-classifier-model/fraud_detector.pkl' before running the test._


----

This file is associated with the book, Building Trustworthy Chatbots: A Risk-aware Approach with Use Cases, by Biplav Srivastava, 2025
