---
title: "How to: Verify VAT Registration Numbers"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: bb720db5-f2fd-4a2f-856c-7a6d379a608f
caps.latest.revision: 4
ms.author: "sgroespe"
translation.priority.ht: 
  - "da-dk"
  - "de-at"
  - "de-ch"
  - "de-de"
  - "en-au"
  - "en-ca"
  - "en-gb"
  - "en-in"
  - "en-nz"
  - "es-es"
  - "es-mx"
  - "fi-fi"
  - "fr-be"
  - "fr-ca"
  - "fr-ch"
  - "fr-fr"
  - "is-is"
  - "it-ch"
  - "it-it"
  - "nb-no"
  - "nl-be"
  - "nl-nl"
  - "ru-ru"
  - "sv-se"
---
# How to: Verify VAT Registration Numbers
You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.  
  
 When you modify the **\($ T\_18\_86 VAT Registration No. $\)** field on a card where the value in the **\($ T\_18\_35 Country\/Region Code $\)** field is an EU country\/region, then the new VAT registration number and your user ID are logged in the **\($ N\_249 VAT Registration Log $\)** window. You verify a VAT registration number by choosing the **Verify Registration No.** button in the **\($ N\_249 VAT Registration Log $\)** window. A new line is created every time you use the verification function. If the number could be verified, the **\($ T\_249\_10 Status $\)** field contains **Valid**. If the number could not be verified, the **\($ T\_249\_10 Status $\)** field contains **Invalid**, and you must then change the number in the **\($ T\_18\_86 VAT Registration No. $\)** field on the card and start the verification function again.  
  
 The URL of the default web service is set up in the **\($ T\_98\_161 VAT Reg. No. Validation URL $\)** field in the **\($ N\_118 General Ledger Setup $\)** window.  
  
 In the **\($ T\_381 VAT Registration No. Format $\)** table, you can change for each country\/region the different formats of VAT registration number that users are allowed to enter in the **\($ T\_18\_86 VAT Registration No. $\)** field.  
  
> [!WARNING]  
>  This web service uses the http protocol, which means that data transferred through the service is not encrypted.  
  
> [!NOTE]  
>  You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.  
  
### To verify a VAT registration number from a customer card  
  
1.  In the **Search** box, enter **Customers**, and then choose the related link.  
  
2.  Open the card of a customer where you want to verify the VAT registration number.  
  
    > [!NOTE]  
    >  The **\($ T\_18\_35 Country\/Region Code $\)** field on the customer card must contain an EU country\/region.  
  
3.  On the **Foreign Trade** FastTab, choose the DrillDown button next to the **\($ T\_18\_86 VAT Registration No. $\)** field.  
  
     The **\($ N\_249 VAT Registration Log $\)** window opens showing one line where the **\($ T\_249\_10 Status $\)** field contains **Not Verified**.  
  
4.  On the **Home** tab, in the **Process** group, choose **Verify Registration No.**.  
  
     A new line is created where the **\($ T\_249\_10 Status $\)** field contains either **Valid** or **Invalid**.  
  
5.  If the **\($ T\_249\_10 Status $\)** field contains **Invalid**, change the number in the **\($ T\_18\_86 VAT Registration No. $\)** field on the card, and then repeat steps 3 through 4.  
  
## See Also  
 [\($ N\_249 VAT Registration Log $\)](assetId:///9b93d69a-2f0a-4a31-8eb6-e45a9298e52f)   
 [\($ T\_249 VAT Registration Log $\)](assetId:///30f370f5-17bf-4833-b75e-dfc4b3cbac24)   
 [\($ T\_249\_10 Status $\)](assetId:///32487452-08e0-4136-85e9-83aa8a02d144)   
 [\($ T\_249\_11 Verified Name $\)](assetId:///c269d2a1-5fb2-4ef3-b256-2a142d66d8ac)   
 [\($ T\_18\_86 VAT Registration No. $\)](../Topic/\($%20T_18_86%20VAT%20Registration%20No.%20$\).md)   
 [\($ T\_23\_86 VAT Registration No. $\)](../Topic/\($%20T_23_86%20VAT%20Registration%20No.%20$\).md)   
 [\($ T\_5050\_86 VAT Registration No. $\)](../Topic/\($%20T_5050_86%20VAT%20Registration%20No.%20$\).md)   
 [\($ T\_98\_161 VAT Reg. No. Validation URL $\)](assetId:///f62c95b9-df5a-4389-810b-abfd921d79a1)   
 [\($ T\_381 VAT Registration No. Format $\)](assetId:///9ab10f17-36c6-4ce1-9ca3-0186ecea11d1)