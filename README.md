# How to interact with Coinfirm AML Oracles

## Eth Oracle 

    address: 0x288ff9d5645bb3d246bc0b678621272aec17f9fb

### Using MEW

* enter the [MEW](https://www.myetherwallet.com) website
* create new or access existing wallet ![failed to load image](images/create-or-access-wallet.png)
* add new contract to interact with, set provided `address` and `abi`(content from `eth-oracle.abi`) to relevant placeholders ![faile to load image](images/init-contract.png)
* click `Continue`
* on the right side from contract address, choose 'depositETH' from drop-down menu and set desired amount to deposit (minimal fee for a report 0.001 ETH) ![failed to load image](images/depost-eth.png)
* click `write` and continue with wallet you have signed in; If transaction executes successfully -- your deposit balance will be increased;
* to get default fee choose `getDefaultFee` from drop down menu and copy `Result` value. This is read call, no transaction to be sent ![failed to load iamge](images/default-fee.png)
* next send `askAMLStatus` function, set `maxFee` to value of maximum fee intended to pay for report, has to be greater or equal `default fee` (result from previous point)
 set `target` to the address you want to request AML report generation for; ATTENTION set `Value in ETH field` to ZERO! 
 ![failed to load image](images/ask-aml.png) 
* click `write` and continue with wallet you have signed in; After successful transaction, our platform will generate AML report for the address and set result into blockchain with special transaction. This process is asynchronous, hence client should wait some time;
* next step is to fetch aml status. Choose 'fetchAMLStatus' from drop-down menu and set target to the address you used in previous step. Click write and proceed with the wallet you have signed in;
![failed to load image](images/fetch-aml.png)

* to check deposit ETH balance -- choose `balanceOf` from drop down menu, enter your address in `Account(address) field then click `Read`, the result will appear. This is read call, no transaction to be sent. ![faile to load image](images/balance-of.png)

* to withdraw your depositet ETH, choose `withdrawETH` from drop-down menu, and enter amount to be withdrawn, after click write, and proceed with wallet you have signed in. ![failed to load image](images/withdraw-eth.png)


## AMLT Oracle

    address: 0xb7dcb58da170bbd4831d312b12acf048f8772ae3

### Using MEW

* enter the [MEW](https://www.myetherwallet.com) website
* create new or access existing wallet ![failed to load image](images/create-or-access-wallet.png)
* add new contract to interact with, set provided amlt-oracle `address` and `abi`(content from `amlt-oracle.abi`) to relevant placeholders ![faile to load image](images/init-contract.png)
* on the right side from contract address, choose 'depositAMLT' from drop-down menu and set desired amount to deposit (minimal fee for a report 1 AMLT) ![failed to load image](images/deposit-amlt.png)
* click `write` and continue with wallet you have signed in; If transaction executes successfully -- your deposit balance will be increased;
* to get default fee choose `getDefaultFee` from drop down menu and copy `Result` value. This is read call, no transaction to be sent ![failed to load iamge](images/default-fee-amlt.png)
* next send `askAMLStatus` function, set `maxFee` to value of maximum fee intended to pay for report, has to be greater or equal `default fee` (result from previous point)
 set `target` to the address you want to request AML report generation for; ATTENTION set `Value in ETH field` to ZERO! ![failed to load iamge](images/ask-aml-amlt.png)
* click `write` and continue with wallet you have signed in; After successful transaction, our platform will generate AML report for the address and set result into blockchain with special transaction. This process is asynchronous, hence client should wait some time;
* next step is to fetch aml status. Choose 'fetchAMLStatus' from drop-down menu and set target to the address you used in previous step. Click write and proceed with the wallet you have signed in;
![failed to load image](images/fetch-aml-amlt.png)
* to check deposit AMLT balance -- choose `balanceOf` from drop down menu, enter your address in `Account(address) field then click `Read`, the result will appear. This is read call, no transaction to be sent. ![faile to load image](images/balance-of-amlt.png)

* to withdraw your depositet AMLT, choose `withdrawAMLT` from drop-down menu, and enter amount to be withdrawn, after click write, and proceed with wallet you have signed in. ![failed to load image](images/withdraw-amlt.png)






 
