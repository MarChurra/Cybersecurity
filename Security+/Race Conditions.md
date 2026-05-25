## A Programming conundrum
- Sometimes, things happen at the same time
- This can be bad if you have not planned for it
- Time-of-check to time-of-use attack TOCTOU
  - Check the system
  - When do you sue the results of your last check
  - Something might happen between the check and the use

## Example
- A race condition asumes that deposits to the account are immediate and withdrawals are not
- Starting Account Value:
  - Account A = 100€
  - Account B = 100€
- User 1 transfers 50 from A to B. The Balance is Checked and then the transaction is made
- User 2 transfers 50 from A to . Balance is checked and the transaction is done.
- If done at the same time, if the withdrawal from the account is not handled properly, account A will be left with 50€ instead of 0€.
