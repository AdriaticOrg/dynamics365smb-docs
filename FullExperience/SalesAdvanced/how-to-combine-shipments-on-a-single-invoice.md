---
title: "How to: Combine Shipments on a Single Invoice"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "shipments, combining"
  - "combining, shipments"
ms.assetid: 98f90406-497e-4222-8804-1d653acfe583
caps.latest.revision: 8
ms.author: "sgroespe"
manager: "terryaus"
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
# How to: Combine Shipments on a Single Invoice
If you want to invoice more than one shipment at a time, you can use the combined shipments feature.  
  
 Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted. In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced. To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.  
  
### To manually combine shipments on a single invoice  
  
1.  In the **Search** box, enter **Sales Invoices**, and then choose the related link.  
  
2.  On the **Home** tab, in the **New** group, choose **New**.  
  
3.  In the **Sell\-to Customer No.** field, enter the customer who will receive the invoice for the shipped items.  
  
4.  On the **Lines** FastTab, choose **Actions**![Action Menu icon](../DesignAndEngineering/media/actionmenuicon.png "actionMenuIcon"), choose **Functions**, and then choose **Get Shipment Lines**.  
  
5.  Select the shipment line that you want to include in the invoice:  
  
    -   To insert all lines, select all lines and choose the **OK** button.  
  
    -   To insert specific lines, select the lines and choose the **OK** button. You can use the Ctrl key to select multiple nonsequential lines.  
  
6.  If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re\-run the **Get Shipment Lines** function.  
  
7.  To post the invoice, on the **Actions** tab, in the **Posting** group, choose **Post**.  
  
 If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for invoices in the   **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Post and Print** to print the invoice.  
  
### To automatically combine shipments on a single invoice  
  
1.  In the **Search** box, enter **\($ R\_295 Combine Shipments $\)**, and then choose the related link. The batch job request window opens.  
  
2.  On the **Options** FastTab, fill in the fields. Select the **Post Invoices** field.  
  
3.  Choose the **OK** button.  
  
> [!NOTE]  
>  You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.  
  
## Removing Shipped and Invoiced Orders  
 When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines. The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.  
  
 When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.  
  
#### To remove open sales orders  
  
-   In the **Search** box, enter **Delete Invoiced Sales Orders**, and then select the link.  
  
-   Specify in the **No.** filter field which sales orders to delete.  
  
-   Choose the **OK** button.  
  
 Alternatively, delete individual sales orders manually.  
  
#### To remove open blanket sales orders  
  
-   In the **Search** box, enter **Delete Invoiced Blanket Sales Orders**, and then select the link.  
  
-   Specify in the **No.** filter field which sales orders to delete.  
  
-   Choose the **OK** button.  
  
## See Also  
 [How to: Combine Receipts](../Finance/how-to-combine-receipts.md)   
 [How to: Combine Return Receipts](../Sales/how-to-combine-return-receipts.md)   
 [How to: Combine Return Shipments](../Purchasing/how-to-combine-return-shipments.md)   
 [Processing Sales Orders](../Sales/processing-sales-orders.md)   
 [\($ B\_295 Combine Shipments $\)](../Topic/\($%20B_295%20Combine%20Shipments%20$\).md)   
 [\($ B\_299 Delete Invoiced Sales Orders $\)](../SetupAndAdministration/-$-b_299-delete-invoiced-sales-orders-$-.md)   
 [\($ B\_291 Delete Invd Blnkt Sales Orders $\)](../SetupAndAdministration/-$-b_291-delete-invd-blnkt-sales-orders-$-.md)   
 [Shipping](../Topic/Shipping.md)