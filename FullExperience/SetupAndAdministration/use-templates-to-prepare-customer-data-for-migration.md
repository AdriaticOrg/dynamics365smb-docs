---
title: "Use Templates to Prepare Customer Data for Migration"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "RapidStart Services, migrating data"
ms.assetid: dd6739a4-74a4-46fc-aade-dcbde5fd4fcc
caps.latest.revision: 23
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
# Use Templates to Prepare Customer Data for Migration
After you import and apply setup data in the new database, you can start migrating the customer’s existing master data, such as item and customer numbers and names. To make sure that this data is created quickly and accurately in the new company, you should use templates to structure the data.  
  
 Typically, you create data templates for the following master data tables:  
  
-   **Contact**  
  
-   **Customer**  
  
-   **Item**  
  
-   **Vendor**  
  
 However, you can create a template structure for and apply it to any table in [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)].  
  
> [!TIP]  
>  You can also use data templates for daily operations to create new records that are based on templates. These data templates only work for the supported master data tables. For more information, see [How to: Create Cards by Using Data Templates](../WorkingWithDynamics/how-to-create-cards-by-using-data-templates.md).  
  
 When you import customer data, such as for items, from a file, the mandatory field data that you have specified is taken from the linked data template. When you create a new item, you only enter general information such as item name, description, and price and then collect the rest of the mandatory field data from a selected data template.  
  
 When you create a new master data record, such as a customer card, some fields are mandatory and must be filled in. You can group most mandatory fields, such as posting groups and payment terms, to make creating master data records easier and more stable. For example, you can group mandatory fields for table 18, **Customer**, as **Domestic**, **Foreign**, or **Export** types.  
  
 The following table describes the sequence of tasks with links to topics that describe them. These tasks are listed in the order in which you generally perform them.  
  
|**To**|**See**|  
|------------|-------------|  
|Evaluate configuration data templates and determine whether they meet the customer's needs.|[How to: Select a Configuration Template](../SetupAndAdministration/how-to-select-a-configuration-template.md)|  
|Create new customized templates if the default templates do not meet the customer's needs.|[How to: Create a Configuration Template](../SetupAndAdministration/how-to-create-a-configuration-template.md)|  
|Create a record that is based on a configuration data template.|[How to: Create a Record from a  Configuration Template](../SetupAndAdministration/how-to-create-a-record-from-a-configuration-template.md)|  
|Use a configuration data template on a record.|[How to: Use a Configuration Template on a Record](../SetupAndAdministration/how-to-use-a-configuration-template-on-a-record.md)|  
  
## See Also  
 [Migrate Customer Data](../SetupAndAdministration/migrate-customer-data.md)   
 [Set Up a Company With RapidStart Services for Microsoft Dynamics NAV](../SetupAndAdministration/set-up-a-company-with-rapidstart-services-for-microsoft-dynamics-nav.md)