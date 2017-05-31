---
title: "Payment Scenario 1 - Domestic Payments (LCY to LCY)"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "payment scenarios, domestic"
ms.assetid: 6727f31b-c9f6-49d5-8104-688fde627b91
caps.latest.revision: 9
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "nl-nl"
---
# Payment Scenario 1 - Domestic Payments (LCY to LCY)
You can use telebanking for trade with domestic and foreign customers and vendors. This topic describes a scenario where the trade is with domestic customers and vendors.  
  
 The following list describes the main steps:  
  
1.  Create Vendor\/Customer.  
  
2.  Create Vendor\/Customer Bank Account.  
  
3.  Create and Post Purchase Invoice for Vendor or Sales Invoice for Customer.  
  
4.  Create Proposal.  
  
5.  Create Payment History.  
  
6.  Export Payment History.  
  
7.  Import Bank Statement.  
  
> [!NOTE]  
>  In the examples below some standard CRONUS data is being used. Likewise instead of creating a vendor\/customer and a vendor\/customer bank account you could use existing data.  
  
## Create Vendor\/Customer  
 Create vendor\/customer and enter all necessary information. Special attention should be paid to:  
  
-   **Currency Code**: leave empty \- i.e. it is set to the local currency \(LCY\).  
  
-   **Transaction Mode**: select an appropriate, default transaction mode \- i.e. one that can deal with local currency payments for your bank.  
  
-   **\($ T\_23\_288 Preferred Bank Account $\)**: select an appropriate, default vendor\/customer bank account having the same Currency Code as the vendor\/customer itself.  
  
> [!NOTE]  
>  In order to be able to enter a bank account in the **Bank Account** vendor\/customer bank accounts must be available. See below.  
  
### Example  
 Olek Johansson \(code *OLEK*\) is one of our local vendors. Purchase invoices will be paid through our national bank account \(code *ABN*\) to his bank account \(code *OJBA*\). Both bank account ABN and OJBA are denominated in local currency \(LCY\). Therefore on Olek Johansson's Vendor Card we leave the *Currency Code* field empty, fill the *Transaction Mode* field with *ABN* that is linked to our bank account *ABN* and set the *Bank Account* field to *OJBA*.  
  
## Create Vendor\/Customer Bank Account  
 Create vendor\/customer bank account and enter all necessary information. Special attention should be paid to:  
  
-   **\($ T\_23\_288 Preferred Bank Account $\)**: enter a valid bank account number.  
  
-   **Currency Code**: leave empty \- i.e. it is set to the local currency \(LCY\).  
  
-   **Owner Information**:be sure all owner information has been entered.  
  
### Example  
 Olek Johansson's bank account \(code *OJBA*\) is denominated in local currency \(LCY\). Therefore on Olek Johansson's Vendor Bank Account Card we enter a valid number in the *Bank Account No.* field *,* leave the *Currency Code* field empty and fill the fields on the Owner Information tab with appropriate values.  
  
## Create and Post Purchase Invoice for Vendor or Sales Invoice for Customer  
 Create a purchase\/sales invoice and enter all necessary information. Special attention should be paid to:  
  
-   **Currency Code**: leave empty \- i.e. it is set to the local currency \(LCY\).  
  
-   **Transaction Mode**: select an appropriate, default transaction mode \- i.e. one that can deal with local currency payments for your bank.  
  
-   **\($ T\_23\_288 Preferred Bank Account $\)**: select an appropriate, default vendor\/customer bank account having the same Currency Code is the vendor\/customer itself.  
  
 By default these three fields will be populated with values taken from the vendor\/customer card.  
  
 When the invoice is finished it can be posted.  
  
### Example  
 When creating a purchase invoice for Olek Johansson we enter *OLEK* in the ***Buy\-from Vendor No.*** field. By default the *Currency Code*, *Transaction Mode* and *Bank Account* fields will be populated with values taken from the Olek Johansson's vendor card. Therefore the *Currency Code*, *Transaction Mode* and *Bank Account* fields will be *\<empty\>*, *ABN* and *OJBA* respectively. Nevertheless, these values can be changed.  
  
## Create Proposal  
 Open the [\($ N\_11000000 Telebank \- Bank Overview Window $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Netherlands/-$-n_11000000-telebank-bank-overview-window-$-.md) window and browse to the bank through which we want to perform our payment. Open the Proposal window and generate payment proposals using the Get Proposal Entries batch job.  
  
### Example  
 Through the Telebank \- Bank Overview window we open the Proposal window for our bank *ABN*. Using the batch job one proposal line will be created for the purchase invoice we just created and posted for vendor *OLEK*.  
  
## Create Payment History  
 From the Proposal window we process our proposal into a payment history. The proposal will disappear and can be found in the Payment History Overview window for the same bank.  
  
### Example  
 We process our proposal concerning the payment to vendor *OLEK* and open the Payment History Overview window for our bank *ABN*. The last payment history is the one we just created.  
  
## Export Payment History  
 Open the [\($ N\_11000007 Payment History Overview Window $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Netherlands/-$-n_11000007-payment-history-overview-window-$-.md) window, browse to the relevant payment history and choose **Export**. The export batch job will appear for the export protocol that is linked to this payment. For this export the system already has entered appropriate filters. Check, if wanted, any of the fields on the Options tab and click OK to export the payment. The system will generate a text file using a filename as defined in the [\($ T\_11000005\_21 Default File Names Field $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Netherlands/-$-t_11000005_21-default-file-names-field-$-.md) field of the export protocol, which now is ready to be sent to our bank.  
  
### Example  
 As the transaction mode associated with our payment is *ABN* the CLIEOP03 batch job will appear.  
  
## Import Bank Statement  
 After receiving electronic bank statements from our bank we can import them by running the appropriate import protocol from the Import Protocol List window.  
  
### Example  
 The bank statement containing our payment to Olek Johansson will be sent to us by our bank *ABN*. Therefore we should chose *OFFICE NET EXTRA* as the appropriate import protocol.  
  
## See Also  
 [How to: Create Proposals](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Netherlands/how-to-create-proposals.md)   
 [How to: Create and Export Payment History](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Netherlands/how-to-create-and-export-payment-history.md)