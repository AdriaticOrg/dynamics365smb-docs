---
title: "How to: Set Up Vendors for Remittance"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "vendors, remittance"
  - "remittance, vendors"
ms.assetid: 74aaf111-ad60-48c7-b623-6b079b63904c
caps.latest.revision: 2
ms.author: "edupont"
translation.priority.ht: 
  - "nb-no"
---
# How to: Set Up Vendors for Remittance
[!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] includes Norwegian enhancements for automatically making payments to vendors. This reduces errors that occur from manual data entry. To pay vendors using the remittance system, you must set up vendor information.  
  
### To set up a vendor for remittance  
  
1.  In the **Search** box, enter **Vendors**, and then choose the related link.  
  
2.  Select the vendor, and on the **Home** tab, choose **Edit**.  
  
3.  On the **General** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_23\_2 Name $\)**|Specify the vendor’s name. This field is used by remittance against Bankernes Betalingssentral \(BBS\).|  
    |**\($ T\_23\_5 Address $\)**|Specify the vendor’s address. This field is used by remittance against BBS.|  
    |**\($ T\_23\_6 Address 2 $\)**|Specify an additional line for the vendor’s address, if necessary. This field is used by remittance against BBS.|  
    |**\($ T\_23\_91 Post Code $\)**|Specify a valid postal code of four digits for domestic remittance.|  
    |**\($ T\_23\_35 Country\/Region Code $\)**|Specify a valid country\/region code for a foreign address.|  
  
4.  On the **Payments** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_23\_15000000 Remittance $\)**|Select if the vendor is to be remitted.|  
    |**\($ T\_23\_15000001 Remittance Account Code $\)**|Specify the account code to be used for the vendor.|  
    |**\($ T\_23\_15000002 Recipient Bank Account No. $\)**|Specify the account number used to remit the vendor.|  
  
5.  On the **Navigate** tab, in the **Vendor** group, choose **Remittance Info**.  
  
6.  On the **General** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_23\_15000001 Remittance Account Code $\)**|Specify the code of the remittance account which the vendor is using.|  
    |**\($ T\_23\_15000003 Remittance Agreement Code $\)**|Specify the code of the agreement to which the account is linked.|  
    |**\($ T\_23\_15000002 Recipient Bank Account No. $\)**|Specify the vendor's account number used for remittance.|  
  
7.  On the **Domestic** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_23\_15000031 Own vendor recipient ref. $\)**|Select to use the recipient reference from the vendor.|  
    |**\($ T\_23\_15000005 Recipient ref. 1 \-\- inv. $\)**|Enter the text that will print on the payment invoice.|  
    |**\($ T\_23\_15000008 Recipient ref. 1 \- cred. $\)**|Enter the text that will print on the payment invoice when deducting a credit memo.|  
  
     If remittance to BBS is used, the text from **Recipient ref. \- inv.** and **Recipient ref. \-cred.** is displayed on the payment specification in lines one through three, columns one and two. You can insert a maximum of 80 characters on the payment specification.  
  
     The text in the recipient reference fields can be formatted automatically with special codes. For more information, see [Recipient Reference Codes](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/recipient-reference-codes.md).  
  
8.  On the **Payment abroad** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_23\_15000026 Recipient Ref. Abroad $\)**|Enter the text that will print on the payment invoice.|  
    |**\($ T\_23\_15000013 Warning Notice $\)**|Select one of the following options to specify how a warning notice is sent from the recipient's bank to the recipient.<br /><br /> -   **None** \- No confirmation is sent.<br />-   **Phone** \- Confirmation is given by phone.<br />-   **Fax** \- Confirmation is sent by fax.<br />-   **Other** \- A text message in the **Warning Text** field is used.|  
    |**\($ T\_23\_15000014 Warning Text $\)**|Enter the warning text that is used if the **Warning Notice** field is set to **Other**.|  
    |**\($ T\_23\_15000022 Recipient Confirmation $\)**|Select to specify how confirmation of payment is sent to the recipient.|  
    |**\($ T\_23\_15000023 Telex Country\/Region Code $\)**|Specify the country\/region code if the confirmation is sent using telex.|  
    |**\($ T\_23\_15000024 Telex\/Fax No. $\)**|Specify the telex or fax number if the confirmation is sent using telex or fax.|  
    |**\($ T\_23\_15000025 Recipient Contact $\)**|Specify the contact person’s name if a telex or fax confirmation is sent to the recipient.|  
    |**\($ T\_23\_15000012 Charges Domestic $\)**|Specify who is charged the domestic charges in connection with the payment.<br /><br /> -   **Debitremitter** \- The remitter is charged.<br />-   **Debitrecipient** \- The recipient is charged.<br />-   **Default** \- The bank's way of charging is used. Typically this is the remitter who is charged.|  
    |**\($ T\_23\_15000030 Charges Abroad $\)**|Specify who is charged for foreign payments.<br /><br /> -   **Debitremitter** \- The remitter is charged.<br />-   **Debitrecipient** \- The recipient is charged.<br />-   **Default** \- The bank's way of charging is used. Typically this is the remitter who is charged.|  
    |**\($ T\_23\_15000027 Payment Type Code Abroad $\)**|Enter a two\-digit code for the payment type.|  
    |**\($ T\_23\_15000028 Specification \(Norges Bank\) $\)**|Specify information for your local government bank. Contact your bank for further information.|  
  
9. On the **Bank abroad** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_23\_15000015 SWIFT $\)**|Enter the Society for Worldwide Interbank Financial Telecommunication \(SWIFT\) address by which the recipient’s bank is identified.|  
    |**\($ T\_23\_15000016 Bank Name $\)**|Specify the bank's name.|  
    |**\($ T\_23\_15000017 Bank Address 1 $\)**|Specify the address of the recipient's bank.|  
    |**\($ T\_23\_15000021 Rcpt. Bank Country\/Region Code $\)**|Specify the country\/region code for the recipient. This field is required and must comply with ISO standards.|  
    |**\($ T\_23\_15000020 SWIFT Remb. Bank $\)**|Specify the SWIFT address for reimbursement that is the recipient’s corresponding bank.|  
  
10. Choose the **OK** button.  
  
## See Also  
 [Electronic Payments to Vendors in Norway](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/electronic-payments-to-vendors-in-norway.md)   
 [How to: Set Up Remittance Agreements](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-set-up-remittance-agreements.md)   
 [How to: Create Remittance Accounts](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-create-remittance-accounts.md)   
 [Recipient Reference Codes](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/recipient-reference-codes.md)   
 [How to: Create Remittance Suggestions](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-create-remittance-suggestions.md)   
 [How to: Create Manual Remittance Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-create-manual-remittance-payments.md)   
 [How to: Set Up Payment Line Information](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-set-up-payment-line-information.md)   
 [How to: Test Remittance Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-test-remittance-payments.md)   
 [How to: Export Remittance Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-export-remittance-payments.md)   
 [Types of Payment Returns Files](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/types-of-payment-returns-files.md)   
 [How to: Import Payment Return Data](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-import-payment-return-data.md)   
 [How to: Delete Remittance Payment Orders](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-delete-remittance-payment-orders.md)   
 [Remittance Errors](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/remittance-errors.md)   
 [How to: View Remittance Error Codes](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-view-remittance-error-codes.md)   
 [How to: Cancel Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Norway/how-to-cancel-payments.md)