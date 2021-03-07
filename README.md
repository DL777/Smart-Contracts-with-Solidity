# Smart Contracts with Solidity

In this project, I programmed three contracts for hypothetical compensation arrangements that may be set up by a company HR:

- `AssociateProfitSplitter` contract that accepts ETH into the contract and divides it evenly among associate-level employees. This will allow the human resources department to pay employees quickly and efficiently. 

- `TieredProfitSplitter` contract that distributes different percentages of incoming ETH to employees at different tiers/levels. For example, the CEO gets paid 60%, CTO 25%, and Bob gets 15%.

- `DeferredEquityPlan` contract that models traditional company stock plans. This contract will automatically manage 1000 shares, with an annual distribution of 250 shares over four years for a single employee.

# Associate Profit Splitter

This hypothetical contract is setup to facilitate the payment to three associate-level employees who are all paid the equal share of all ETH transferred into the contract. The contract can be scaled up to facilitate the payments to a large group of employees. 

The Solidity code is shown in this screenshot:

![Contract1](Screenshots/Contract1.png)

The contract was originally deployed in `Remix` on my local  `Ganache` chain by connecting to `Injected Web3` and ensuring `MetaMask` is pointed to `localhost:8545`.


This contract was deployed from my `Account 4` on my local `Ganache` chain and my `Account 1`, `Account 2` and `Account 3` were designated as `employee_one`, `employee_two` and `employee_three` respectively.

![cont1deploy_local](Screenshots/c1d.png)


Here is the screenshot of the balance in my `Account 4` (HR) and my "employee" accounts before the the deposit of funds:

![Contract1_accbefore](Screenshots/c1accbefore.png)

I booked a deposit transaction for ETH 30:

![cont1_tx](Screenshots/c1_tx.png)
![cont1_tx](Screenshots/c130eth.png)

And the balances in my accounts changed accordingly:

- The balance in Account 4 decreased by ETH30 and 
- The balances in my Account1, Account 2 and Account 3 increased by ETH 10 each:

![cont1_tx](Screenshots/c1accafter.png)

Following this, I deployed `AssociateProfitSplitter` contract on `Ropsten Test Network`:
![cont1_tx](Screenshots/c1ropsten.png)

The contract address is `0x58d586456b5d8D9Da820097a63d83692e78d6f9D` and it can be checked on Etherscan:

![Contract1_On_Kovan](Screenshots/Cont1Kovan.png)

# Tiered Profit Splitter

This hypothetical contract is setup to facilitate the payments to three employees of different seniority who are paid different percentages of incoming ETH payments. In this example the employees are:

- The CEO, who gets paid 60%, 
- The CTO, who gets paid 25% and
- Bob, who gets paid 15%.

The Solidity code is shown in this screenshot:

![Contract1](Screenshots/c2.png)

Just like in the first contract, I first set up the contract on my local chain and then deployed it on ‘Ropsten Test Network`.

This contract was deployed from my `Account 4` on my local `Ganache` chain and my `Account 1`, `Account 2` and `Account 3` were designated as `employee_one (CEO)`, `employee_two (CTO)` and `employee_three (Bob)` respectively.


![cont1deploy_local](Screenshots/c2d.png)

I booked a deposit transaction for ETH 30:
![c2tx](Screenshots/c2tx.png)

![cont1_tx](Screenshots/c2before.png)

And the balances in my accounts changed accordingly:

- The balance in Account 4 decreased by ETH30 and 
- The balance in my Account1 increased by ETH 18,
- The balance in my Account 2 increased by ETH 7.5,
- The balance in my Account 3 increased by ETH 4.5.

![cont2_after](Screenshots/c2after.png)

Following this, I deployed `TieredProfitSplitter` contract on `Ropsten Test Network`:
![cont1_tx](Screenshots/c2ropsten.png)

The contract address is `0x1e0692d65a229D987eC0C48a9C9D13Bf82e9d333` and it can be checked on Etherscan:

![Contract1_On_Ropsten](Screenshots/c2etherscan.png)