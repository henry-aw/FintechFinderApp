# *Module 19 Challenge*
## Fintech Finder: An Application for Finding, Hiring and Paying Fintech Professionals

**Welcome to my Module 19 Challenge repository.  Here, you can checkout the the disruptive platform, Fintech Finder: an application that customers can use to find fintech professionals from among a list of candidates, hire them, and pay them, with integration of the Ethereum blockchain network in order to enable customers to send cryptocurrency payments.  Find out more in the following sections!**

---

## Background
This project has been completed using two Python files.  The first file  is called fintech_finder.py, and it contains the code associated with the web interface of my application.  The code included in this file is compatible with the Streamlit library.  The second file used is called crypto_wallet.py, and it contains the Ethereum transaction functions that I created throughout the lessons of this module.  By using import statements, I integrated the crypto_wallet.py Python script into the Fintech Finder interface program that is found in the fintech_finder.py file.  Integrating these two files allowed me to automate the tasks associated with generating a digital wallet, accessing Ethereum account balances, and signing and sending transactions via Ethereum's Kovan testnet.

For this project, I acted as a Blockchain Engineer as a startup that is building a new and disruptive platform called Fintech Finder.  Fintech Finder is an application that its customers can use to find fintech professionals from among a list of candidates, hire them, and pay them.  As Fintech Finder's lead developer, I had the task of integrating the Ethereum blockchain network into the application in order to enable my customer to send cryptocurrency payments to fintech professionals.  To develop the code and test it out, I had to assume the perspective of a Fintech Finder customer who is using the application to find a fintech professional and pay them for their work.

Specifically, I assumed the perspective of a Fintech Finder customer in order to do the following:
- Generate a new Ethereum account instance by using my mneumonic seed phrase (which I created earlier in this module).
- Fetch and display the account balance associated with my Ethereum account address.
- Calculate the total value of an Ethereum transaction, including the gas estimate, that pays a Fintech Finder candidate for their work.
- Digitally sign a transaction that pays a Fintech Finder candidate, and send this transaction to the Kovan testnet.
- Review the transaction hash code associated with the validated blockchain transaction.

Once I received the transaction's hash code, I navigated to Kovan's Etherscan website to review the blockchain transaction details.  I have include screenshots of the deployed aaplication and the Etherscan transaction log below.

---

## Streamlit Application
The deployed streamlit application looks like this:
![Screen Shot 2021-11-09 at 5 22 58 PM](https://user-images.githubusercontent.com/86025349/141018665-7fe7d720-b67e-49d3-9db0-b961a4af5ced.png)

I provided some sample input to demonstrate how the application functions when a candidate is selected for hire and paid for their work:
![Screen Shot 2021-11-09 at 5 22 25 PM](https://user-images.githubusercontent.com/86025349/141018603-1b5513d5-ebe0-4c29-85b6-1e722bf594f4.png)
As the transaction was successfully communicated to the Ethereum Kovan testnet, validated, and added to a block, a resulting transaction hash was written to the Streamlit application sidebar.

## Etherscan Transaction Log
My address balance and history of Etherscan looks like this:
![Screen Shot 2021-11-09 at 5 19 22 PM](https://user-images.githubusercontent.com/86025349/141018846-66d1d656-2bc8-4140-946f-e1903a94c99b.png)

The transaction details on Etherscan look like this:
![Screen Shot 2021-11-09 at 5 20 42 PM](https://user-images.githubusercontent.com/86025349/141018874-31519695-7ffe-4e88-ab84-fe79b746473a.png)

The recipient's address balance and history on Etherscan look like this:
![Screen Shot 2021-11-09 at 5 21 25 PM](https://user-images.githubusercontent.com/86025349/141018894-a5c1eb35-eac0-4a92-9e86-4169352c1bb7.png)

---

## Technologies and Usage
This project leverages Python 3.8.8, Streamlit, Web3 and the dataclasses and bip44 libraries with the following requirements and dependencies:

**for crypto_wallet.py:**
- import os
- import requests
- from dotenv import load_dotenv
- load_dotenv()
- from bip44 import Wallet
- from web3 import Account
- from web3.auto.infura.kovan import w3
- from web3 import middleware
- from web3.gas_strategies.time_based import medium_gas_price_strategy

**for fintech_finder.py**
- import streamlit as st
- from dataclasses import dataclass
- from typing import Any, List





