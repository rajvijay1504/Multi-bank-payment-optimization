# Multi-bank-payment-optimization

Welcome to the Multi-Bank Payment Optimization System README!

This system streamlines transactions among multiple banks worldwide, each operating with distinct payment methodologies. Acting as an intermediary between banks with diverse payment modes, the Reserve Bank of India (RBI) facilitates efficient fund transfers.

## Getting Started

Consider the following example with a variety of banks:

1. RBI (Intermediary Bank)
2. AXIS Bank
3. State Bank of India (SBI Bank)
4. ICICI Bank
5. Bank of Baroda
6. HDFC Bank

And the accompanying transactions:

| Debtor Bank           | Creditor Bank          | Amount (Rs) |
|-----------------------|------------------------|-------------|
| HDFC Bank             | RBI                    | 100         |
| HDFC Bank             | AXIS Bank              | 300         |
| HDFC Bank             | SBI Bank               | 100         |
| HDFC Bank             | ICICI Bank             | 100         |
| Bank of Baroda        | RBI                    | 300         |
| Bank of Baroda        | SBI Bank               | 100         |
| RBI                   | AXIS Bank              | 400         |
| AXIS Bank             | SBI Bank               | 200         |
| SBI Bank              | ICICI Bank             | 500         |

These transactions are depicted as a directed graph, where each edge denotes a financial obligation.

![image](https://github.com/rajvijay1504/Multi-bank-payment-optimization/assets/120421407/5725ff12-387a-4839-bb3a-9d5dc253d784)


However, there's a twist! Each bank exclusively supports specific payment modes, limiting transactions to those methods. Only the RBI accommodates all payment modes. In this scenario, we have three payment modes: Google_Pay, Bharat_Pay, and Paytm.

Here are the banks and their supported payment modes:

- RBI: Google_Pay, Bharat_Pay, Paytm
- AXIS Bank: Google_Pay, Bharat_Pay
- SBI Bank: Bharat_Pay
- ICICI Bank: Google_Pay, Paytm
- Bank of Baroda: Bharat_Pay, Paytm
- HDFC Bank: Paytm

## Algorithm Overview

1. Compute the net amount for each bank.
2. Identify the bank with the minimum net amount (max debtor) and the bank with the maximum net amount (max creditor) with a shared payment mode.
3. Execute the transaction between these banks.
4. Repeat the process until all transactions are resolved.

For our example, the optimized payment flow among Indian banks results in the following transactions:

![image](https://github.com/rajvijay1504/Multi-bank-payment-optimization/assets/120421407/b6f7ec1d-18d4-4c7c-8cb1-62e4ad28d5b6)


