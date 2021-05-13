# stateful
Algorand Stateful Smart Contracts
https://developer.algorand.org/docs/features/asc1/stateful/

Algorand Smart Contracts can be written in either a stateless or stateful manner. To be stateful means that some amount of storage on the chain is used to store values. This storage can be either global or local. Local storage refers to storing values in an accounts balance record if that account participates in the contract. Global storage is data that is specifically stored on the blockchain for the contract globally. Like stateless smart contracts, stateful contracts are written in TEAL and can be deployed to the blockchain using either the goal command-line tool or the SDKs. Stateless smart contracts’ primary purpose is to approve or reject spending transactions. Stateful contracts do not approve spending transactions but provide logic that allows the state (globally or locally) of the contract to be manipulated. 

https://developer.algorand.org/docs/features/asc1/stateless/

Stateless Contract Account

For each unique compiled stateless smart contract program there exists a single corresponding Algorand address, output by goal clerk compile. To use a TEAL program as a contract account, send Algos to its address to turn it into an account on Algorand with a balance. Outwardly, this account looks no different from any other Algorand account and anyone can send it Algos or Algorand Standard Assets to increase its balance. The account differs in how it authenticates spends from it, in that the logic determines if the transaction is approved. To spend from a contract account, create a transaction that will evaluate to True against the TEAL logic, then add the compiled TEAL code as its logic signature. It is worth noting that anyone can create and submit the transaction that spends from a contract account as long as they have the compiled TEAL contract to add as a logic signature. Contract accounts are great for setting up escrow style accounts where you want to limit withdrawals or you want to do periodic payments

https://developer.algorand.org/docs/features/asc1/stateless/modes/
