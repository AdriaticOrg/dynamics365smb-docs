---
title: "How to: Replan Production Orders"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "production orders, replanning"
  - "planning, replanning"
ms.assetid: e677bb04-50c1-4127-bd2b-5816e234166d
caps.latest.revision: 15
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
# How to: Replan Production Orders
This planning function calculates changes made to components and routings lines, and it includes items on lower production BOM levels for which it may generate new production orders.  
  
 Based on the changes you have made to the components and routing lines, the **Replan** function calculates and plans for any new demand for the production order. It is typically used after you have added or changed components that constitute underlying production orders.  
  
> [!NOTE]  
>  To include changes made to the header, you must first refresh the production order. For more information, see [How to: Refresh Production Orders](../OperationsPlanning/how-to-refresh-production-orders.md).  
  
### To replan a production order  
  
1.  In the **Search** box, enter **Production Orders**, and then choose the related link.  
  
2.  Select the production order you want to replan.  
  
3.  On the **Lines** FastTab, choose **Actions** , choose **Lines**, and then choose **Components**.  
  
4.  Add a component, which is a produced item or subassembly.  
  
5.  From the production order, on the **Actions** tab, in the **Functions** group, choose **Replan**.  
  
     In the **Replan Production Order** window, define how and what to replan.  
  
6.  In the **Scheduling Direction** field, select one of the following options.  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------------------------------|  
    |**Back**|Calculates the operation sequence backwards from the earliest possible ending date, defined by due date and\/or other scheduled orders, to the latest possible starting date. **Note:**  This default option is relevant in the majority of situations.|  
    |**Forward**|Calculates the operation sequence forward from the earliest latest possible starting date, defined by due date and\/or other scheduled orders, to the earliest possible ending date. **Note:**  This option is only relevant for expedite orders.|  
  
7.  In the **Plan** field, select whether to calculate production requirements for produced items on the production BOM, as follows.  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------------------------------|  
    |**No Levels**|Do not consider lower level production. This only updates the item’s schedule, like refresh.|  
    |**One Level**|Plan for first\-level production demand. First\-level production orders may be created.|  
    |**All Levels**|Plan for all\-level production demand. All\-level production orders may be created.|  
  
8.  Select **One Level**, and choose the **OK** button to replan the production order, and calculate and create a new underlying production order for the introduced subassembly, if it is not fully available.  
  
> [!NOTE]  
>  Changes implemented with the **Replan** function are very likely to change the capacity need of the production order and you may therefore have to reschedule operations afterwards.  
  
## See Also  
 [How to: Refresh Production Orders](../OperationsPlanning/how-to-refresh-production-orders.md)   
 [How to: Plan for New Demand](../OperationsPlanning/how-to-plan-for-new-demand.md)   
 [About Production Orders](../Production/about-production-orders.md)