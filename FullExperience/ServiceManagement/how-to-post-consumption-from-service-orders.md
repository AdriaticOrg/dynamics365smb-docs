---
title: "How to: Post Consumption from Service Orders"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "posting, service consumptions"
  - "service consumptions, posting"
  - "consumption, posting from service orders"
  - "service posting, consumption"
ms.assetid: 6feed7e2-f7fd-497d-8830-11481a415c47
caps.latest.revision: 7
ms.author: "edupont"
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
# How to: Post Consumption from Service Orders
The following procedure describes how to post the items, resource hours, and or costs used for a specific service operation for which you will not charge your customer. It is not possible to post consumption before posting shipment and you cannot post consumption for lines where all quantity shipped has already been invoiced. Note that you can post consumed items, hours, or costs only for a posted shipment that has no posted invoices or consumption.  
  
### To post consumption from a service order  
  
1.  In the **Search** box, enter **Service Orders**, and then choose the related link.  
  
2.  Open the service order you want to post consumption for.  
  
3.  On the **Lines** FastTab, select the service item. Choose **Actions**![Action Menu icon](../DesignAndEngineering/media/actionmenuicon.png "actionMenuIcon"), choose **Order**, and then choose **Service Lines**.  
  
4.  In the **Service Lines** window, find the required entries and specify in the **Qty. to Consume** field the quantities for which you will post consumption. Tthe quantity cannot be larger than the quantity already shipped and the quantity remaining not invoiced after partial invoicing of this shipment.  
  
    > [!NOTE]  
    >  To register consumption with respect to a job, fill in the **Job No.**, **Job Task No.**, and the **Job Line Type** fields on the service line.  
  
5.  Select the lines you want to post, and on the **Actions** tab, in the **Posting** group, choose **Post**. In the window that opens, select **Ship and Consume**.  
  
 The service is posted as consumed either partially or fully, depending on the value in the **Qty. to Consume** field, and the relevant ledger entries are created. In addition, previously posted service shipment documents are updated chronologically with the consumed quantities. The relevant quantities will be updated on the service lines of the order.  
  
## See Also  
 [How to: Post Shipments from Service Orders](../Service/how-to-post-shipments-from-service-orders.md)   
 [How to: Post Invoices from Service Orders](../Service/how-to-post-invoices-from-service-orders.md)   
 [How to: Undo Service Consumption](../Service/how-to-undo-service-consumption.md)