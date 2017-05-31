---
title: "How to: Register Quantity Adjustments in Warehouse Item Journals"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "adjusting, bin quantities"
  - "bin contents, discrepancies"
  - "registering, quantity adjustments"
  - "bin quantity adjustments, registering in warehouse item journals"
ms.assetid: 02e8fd31-f625-4286-9c2f-6ecc3c348925
caps.latest.revision: 10
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
# How to: Register Quantity Adjustments in Warehouse Item Journals
If your location uses directed put\-away and pick, use the **Whse. Item Journal** to post, outside the context of the physical inventory, all positive and negative adjustments in item quantity that you know are real gains, such as items previously posted as missing that show up unexpectedly, or real losses, such as breakage.  
  
 Unlike posting adjustments in the inventory item journal, using the warehouse item journal gives you an additional level of adjustment that makes your quantity records even more precise at all times. The warehouse thus always has a complete record of how many items are on hand and where they are stored, but each adjustment registration is not posted immediately to the item ledger. In the registering process, credits or debits are made to the real bin with the quantity adjustment and a counterbalancing entry is made in an adjustment bin, a virtual bin with no real items. This bin is defined during in the **\($ T\_14\_7317 Invt. Adjustment Bin Code $\)** on the location card. At regular intervals, you synchronize warehouse entries with the item ledger. For more information, [How to: Post Quantity Adjustments for Bins](../WarehouseActivities/how-to-post-quantity-adjustments-for-bins.md).  
  
> [!NOTE]  
>  If the location does not use directed put\-away and pick, simply use the **\($ N\_40 Item Journal $\)** to post, outside the context of the physical inventory, all positive and negative adjustments in item quantity that you know are real gains or real losses. In that case, no adjustment with warehouse entries is required.  
  
### To register a discrepancy in item quantity  
  
1.  In the **Search** box, enter **\($ N\_7324 Whse. Item Journal $\)**, and then choose the related link.  
  
2.  Fill in the header information.  
  
3.  Fill in the **Item No.** field on the line.  
  
4.  Enter the bin in which you are putting the extra items or where you have found items to be missing.  
  
5.  Fill in the quantity that you observe as a discrepancy in the **Quantity** field. If you have found extra items, enter a positive quantity. If items are missing, enter a negative quantity.  
  
6.  On the **Actions** tab, in the **Registering** group, choose **Register.**  
  
#### Example  
 You find a few units of an item on a fork lift truck. You do not know where the units should be stored, but you can place them in a bin and register the quantity to this bin in the **\($ N\_7324 Warehouse Item Journal $\)** window. When you do this, a positive quantity is registered to the bin in which you have placed the items, and a negative quantity is registered in the adjustment bin.  
  
 The items found on the truck have most likely been registered to another bin, and at some point, a warehouse employee will observe and register a negative difference in quantity for this bin. Perhaps a pick has been suggested that cannot be fulfilled because items are missing from the bin, or a physical inventory has been performed for the item.  
  
 When the negative adjustment quantity is registered in the **\($ N\_7324 Warehouse Item Journal $\)** window, or a value in the **Qty. \(Phys. Inventory\)** field has been registered in the **\($ N\_7326 Whse. Phys. Invt. Journal $\)** window, a positive counterbalancing entry is made in the adjustment bin.  
  
## See Also  
 [\($ N\_7326 Whse. Phys. Invt. Journal $\)](../Topic/\($%20N_7326%20Whse.%20Phys.%20Invt.%20Journal%20$\).md)   
 [\($ N\_7324 Warehouse Item Journal $\)](../Topic/\($%20N_7324%20Warehouse%20Item%20Journal%20$\).md)   
 [\($ T\_7311\_54 Qty. \(Phys. Inventory\) $\)](../Topic/\($%20T_7311_54%20Qty.%20\(Phys.%20Inventory\)%20$\).md)   
 [Warehouse Adjustment Bin](../WarehouseActivities/warehouse-adjustment-bin.md)   
 [\($ R\_7320 Warehouse Adjustment Bin $\)](../Topic/\($%20R_7320%20Warehouse%20Adjustment%20Bin%20$\).md)   
 [How to: Post Quantity Adjustments for Bins](../WarehouseActivities/how-to-post-quantity-adjustments-for-bins.md)