>   **SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 14      |
|-----------------|
| Student 1 Ayodele Oluwabusola                 |   
| Student 2 Gabriel Gabari             |   
| Student 3 Remi Oyediji               |   
| Student 4 Taiwo Oyewole                |   


**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan	1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing	1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports	1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided	1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned	1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself	1](#_Toc439194683)

# Introduction

This report shares our group's experience testing the ATM simulation system for the Lab. Before this lab, a couple of us mostly knew about software testing from theory. We thought exploratory testing was just a freeform way to check how a system behaves, while manual functional testing seemed more structured, following specific test cases. But doing these tests gave us a much clearer picture. We got hands-on experience with both methods, which helped us understand how they work in real-world software quality assurance.

For our Defect Report, we started with Azure DevOps but unfortunately, the CSV export of the tracked bugs didn't have the adequate presentation of all the important details, so we had to manually log the defects on an Excel sheet. 

# High-level description of the exploratory testing plan

# Test Strategy
Based on the requirements extracted from Appendix B, we outlined the scope, approach, and all testing activities related to the ATM Simulation application. The plan identifies the features to be tested, test types to be performed, and who will be performing each test.
## Scope of Testing
### Features to be Tested
As a team, we’ll be testing the ATM system to ensure it functions as expected. Below is a breakdown of key areas we’ll focus on:  

| **No** | **Test Area** | **What We’re Checking** |  
|------|----------------------|----------------|  
| 1 | System Startup & Shutdown | Make sure the ATM powers on, requests initial cash, and shuts down properly. |  
| 2 | Card Handling | Test if valid/invalid cards are detected and if the ATM retains a card after three failed PIN attempts. |  
| 3 | PIN Validation | Verify correct PIN authentication, how it handles incorrect attempts, and if the system times out when inactive. |  
| 4 | Cash Withdrawal | Ensure withdrawals work only in multiples of $20, check withdrawal limits, insufficient funds handling, and ATM cash availability. |  
| 5 | Deposit Transactions | Confirm that deposits (cash/checks) process correctly, check timeout behavior, and verify manual envelope handling. |  
| 6 | Fund Transfers | Test transferring money between linked accounts, including valid and invalid scenarios. |  
| 7 | Balance Inquiry | Ensure the system correctly displays balances for all account types. |  
| 8 | Transaction Cancellation | Make sure users can cancel at any point during a transaction. |  
| 9 | Receipts & Logging | Verify that receipts print with correct details and that system logs record all transactions properly. |  
| 10 | Error Handling | Check if the system provides clear error messages for invalid inputs, hardware failures, and network issues. |  
| 11 | Grammatical Errors | Look for typos or incorrect wording in system messages. |  
| 12 | Account Type Validation | Make sure the system correctly identifies and displays account types. |  
| 13 | Operator Start/Stop | Ensure operators can securely start and stop the ATM when needed. |  

Each of us ran the same tests to ensure consistency and documented the issues we found. When a test failed, we reported the issue with clear details, including what happened, what we expected, and any patterns we noticed. This way, we tracked defects effectively and also confirmed fixes when we retested.  

The aim is to be thorough but efficient. Catch as many issues as possible while keeping our testing structured and easy to follow.

## Test Types

Two key types of testing were performed to ensure comprehensive coverage of the ATM Simulation Application:



1 Exploratory Testing: Testers performed unscripted testing to explore the ATM software’s behavior and identify potential issues in workflows, error handling, and user experience.


2 Manual Scripted Testing: Detailed test cases will be executed to verify each functional requirement, ensuring that the ATM performs according to specifications (e.g., cash withdrawal, deposits, PIN validation).


## Test Logistics
### Who Will Test Each Functionality
For the Exploratory Testing, it would be a pair testing to be conducted by two members of the team; **Remi and Gabriel**. The same set of tests will be executed. This approach ensures comprehensive coverage from multiple perspectives:

The Manuel Scripted Testing will be executed by the two members of the team as well; **Ayo and Taiwo**.

With this, we ensure that everyone is involved in the testing process and that all aspects of the software, including functionality, usability, and system performance, are validated from diverse viewpoints, leading to more thorough and effective testing.




# Comparison of exploratory and manual functional testing

Text…

-   Note that you need to submit a report generated by your defect tracking
    system, containing all defects recorded in the system.

# Notes and discussion of the peer reviews of defect reports

Brief summary of our Defect Report

- Total Number of Bugs found: 26
- Bugs Resolved: 8
- Unresolved: 18

Just to mention a few, during the peer review, the first pair in our group observed several unusual behaviors in ATM System Version 1.0. One major issue was incorrect transaction calculations.  

For example:  
- Depositing "$100" into a savings account resulted in a balance of "$190", even though the initial balance was "$100".  
- Transferring "$90" from the checking account to the savings account showed "$89.50" on the receipt instead of "$90".  

Initially, we thought the discrepancies might be due to transaction fees. However, since no such charges were mentioned in the system requirements, we reported these cases as bugs.

The second pair in our group observed significant issues with the withdrawal function in ATM System Version 1.0.  

Key findings:  
- Withdrawing $20 or $40 resulted in an extra $20 being dispensed (e.g., $40 for $20, $60 for $40).  
- A $60 withdrawal resulted in $100 being dispensed, with the full amount deducted from the account.  
- However, attempting to withdraw $200 caused the ATM to dispense a $20 bill repeatedly, as long as both the account and the ATM had sufficient funds.  
- Strangely, the $200 withdrawal bug did not affect the account balance but impacted the ATM itself, essentially allowing unlimited withdrawals.  

If this issue existed in a real-world system, it would cause severe financial losses, as the ATM would continue dispensing money without proper deductions. These cases were reported as critical bugs.

In addition to the previously mentioned issues, we also observed anomalies during the Balance Inquiry test.  

One major issue was that when performing a **balance inquiry on the savings account for card 1, the system dispensed "$500", even though it did not have that amount available.  

This unexpected behavior was noted and reported as a critical bug.





# How the pair testing was managed and teamwork/effort was divided 

All team members performed exploratory testing and recorded the defects found. In the end, we all reviewed all defects and reported them in the bug tracking tool. 

# Difficulties encountered, challenges overcome, and lessons learned

Text…

# Comments/feedback on the lab and lab document itself

Text…
