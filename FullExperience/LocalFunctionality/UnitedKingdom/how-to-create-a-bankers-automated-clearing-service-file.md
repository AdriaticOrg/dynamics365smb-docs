---
title: "How to: Create a Bankers&#39; Automated Clearing Service File"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "BACS"
  - "Bankers' Automated Clearing Service (BACS)"
ms.assetid: cd8e1205-6dfa-4c8d-8c3d-df4395ae97ce
caps.latest.revision: 44
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "en-gb"
---
# How to: Create a Bankers&#39; Automated Clearing Service File
In [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)], you can use Bankers' Automated Clearing Service \(BACS\) to process financial transactions electronically. To use BACS as the default vendor payment method, you must set export vendor payments to a BACS file using the **Export BACS** option. The resulting file can then be read by third\-party applications to allow electronic bank payments.  
  
 You can keep track of BACS events, such as exporting and voiding, with the **BACS Ledger Entry** table. You can keep track of BACS transmissions using the **BACS Register** table.  
  
 To create a BACS file, you must follow this sequence of activities:  
  
-   Set up vendor payment information in the **Vendor**  card window.  
  
-   Create the vendor payment using BACS.  
  
-   Export the BACS payment file.  
  
### To set up vendor payment information in the vendor card  
  
1.  In the **Search** box, enter **Vendors**, and then choose the related link.  
  
2.  Select the relevant vendor. On the **Home** tab, choose **Edit**.  
  
3.  On the **Payments** FastTab, in the **\($ T\_23\_10550 BACS Account No. $\)** field, select the BACS account for the vendor.  
  
4.  Choose the **OK** button.  
  
### To create the vendor payment using BACS  
  
1.  In the **Search** box, enter **Vendors**, and then choose the related link.  
  
2.  In the **\($ N\_27 Vendors $\)** window, select the relevant vendor for whom BACS payment was set up in the **Vendor** card window.  
  
3.  To open the **\($ N\_256 Payment Journal $\)** window, on the **Home** tab, in the **Process** group, choose **Payment Journal**.  
  
4.  Fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_81\_7 Document No. $\)**|Specifies the document number for the journal line.|  
    |**\($ T\_81\_3 Account Type $\)**|Select the account type as **Vendor**.|  
    |**\($ T\_81\_4 Account No. $\)**|Specifies the code of the vendor that you selected in the **\($ N\_26 Vendor Card $\)** window.|  
    |**\($ T\_81\_70 Bank Payment Type $\)**|Specifies that the payment type to be used for the entry on the payment journal line is **BACS**.|  
    |**\($ T\_81\_10550 BACS Account No. $\)**|Specifies the BACS account number that you have set on the vendor card.|  
    |**\($ T\_81\_13 Amount $\)**|Specifies the total amount including VAT.|  
  
5.  Choose the **OK** button.  
  
## See Also  
 [How to: Export BACS Files](../../LocalFunctionalityForMicrosoftDynamicsNav2016/UnitedKingdom/how-to-export-bacs-files.md)   
 [\($ T\_10550 BACS Ledger Entry $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/UnitedKingdom/-$-t_10550-bacs-ledger-entry-$-.md)   
 [\($ T\_10551 BACS Register $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/UnitedKingdom/-$-t_10551-bacs-register-$-.md)   
 [\($ N\_256 Payment Journal $\)](../../Finance/-$-n_256-payment-journal-$-.md)   
 [United Kingdom Local Functionality](../../LocalFunctionalityForMicrosoftDynamicsNav2016/UnitedKingdom/united-kingdom-local-functionality.md)