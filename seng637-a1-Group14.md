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

This report shares our group's experience testing the ATM simulation system for the Lab. Before this lab, a couple of us mostly knew about software testing from theory. We thought exploratory testing was just a freeform way to check how a system behaves, while manual functional testing seemed more structured, following specific test cases. But actually doing these tests gave us a much clearer picture. We got hands-on experience with both methods, which helped us understand how they work in real-world software quality assurance.

For our Defect Report, we started out with Azure DevOps but unfortunately, the csv export of the tracked bugs didnt have adequate presentationof all the important details, but we had to manually log the defects on an excel shit. 

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

Each of us will ran the same tests to ensure consistency, and documented the issues we find. When a test failed, we report the issue with clear details, including what happened, what we expected, and any patterns we notice. This way, we can tracked defects effectively and also confirmed fixes when we retest.  

The aim is to be thorough but efficient. Catch as many issues as possible while keeping our testing structured and easy to follow.

## Test Types
Two key types of testing will be performed to ensure comprehensive coverage of the ATM Simulation Application:

1 Exploratory Testing: Testers will perform unscripted testing to explore the ATM software’s behavior and identify potential issues in workflows, error handling, and user experience.


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

Brief sumamary of our Defect Report

- Total Number of Bugs found: 26
- Bugs Resolved: 8
- Unresolved: 18

During our test, the ATM System Version_1.0 responded in a variety of weird ways which was quite fasinating. Just to mention a few, the transaction figures never adds up. For example, when making a deposit of $100, the balance after the deposit in a savings account shows up as $190 in addition to the $100 existing balance. Another scenario is making transfers from one account to the other. Lets say $90 is transferred from Checking account to Saving Account, what shows on the receipt is "$89.50". Discussing these observations as a group, we were under the impression that the difference in amount could be due to transaction charges, but since such was not mentioned in the requirement, these case were reported as bugs.

Also, in the case of making withdrawals, we observed that when withdrawing $20 or $40 bill, the systems adds an additional $20 to the dispenses amount. i.e you get $40 for $20 and $60 for $40 withdrawals. Then in the case of $60 withdrawal, the system dispensed $100. All of these were charged on the account where the withdrawal was iniitied. But the case of withdrawing $200 took a different turn, the ATM system dispensed $20 bill whenever we tried to withdraw $200, as long as there's money in the account, and there's available cash in the system. The funny part of it all is that the bugs for the $200 withdrawals didnt affect the account balance, rather the system itself. If such system were to be released in reality, that would be a major loss to the business, as the ATM would continue spilling money.

For the Balance Inquiry test, we noticed a couple of abnormalies here and there. One of which was that the system dispenses $500 (which the system obviously dont have) when a balance inquiry on the savings account for card 1 was initiated. 





# How the pair testing was managed and team work/effort was divided 

Text…

# Difficulties encountered, challenges overcome, and lessons learned

Text…

# Comments/feedback on the lab and lab document itself

Text…
