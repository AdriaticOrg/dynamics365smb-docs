---
title: "How to: Report Trade with Customers and Vendors in Blacklist Countries-Regions"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "VAT, Blacklist communications"
  - "VAT, reporting trade with certain countries/regions"
  - "VAT reports, reporting trade with certain countries/regions"
ms.assetid: 6c4ecf1e-b473-4406-acf2-44141a22c94a
caps.latest.revision: 18
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "it-it"
---
# How to: Report Trade with Customers and Vendors in Blacklist Countries-Regions
You must submit a periodic report of transactions with customers and vendors in certain countries\/regions that the Italian government has identified in a blacklist. The blacklist communication report must be submitted to the Italian Revenue Agency to help prevent VAT fraud. Transactions that are subject to blacklist reporting include the following:  
  
-   Purchases of goods or services  
  
-   Sales of goods or services  
  
 On a monthly or quarterly basis, you must generate the blacklist communication report for transactions with countries\/regions that have privileged taxation and send it to the Italian Revenue Agency. The Italian Revenue Agency decides which countries\/regions are included on the blacklist. You can view or change countries\/regions on the blacklist by using the **\($ N\_10 Countries\/Regions $\)** window. The periodic report includes only transactions that have an amount above a certain threshold. The threshold amount calculation is applied at the document level. For more information, see the [Italian Revenue Agency](http://go.microsoft.com/fwlink/?LinkId=396483).  
  
 Before you can submit the periodic report, you must set up [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)].  
  
### To update the relevant countries\/regions  
  
1.  In the **Search** box, enter **\($ N\_10 Countries\/Regions $\)**, and then choose the related link.  
  
2.  Choose the relevant country\/region, and then select the **\($ T\_9\_12101 Blacklisted $\)** field.  
  
    > [!NOTE]  
    >  You may not be able to see the **\($ T\_9\_12101 Blacklisted $\)** field. In that case, you must add it to the view.  
  
3.  Enter the **Foreign Country\/Region Code** for the blacklisted country\/region.  
  
 For a list of relevant countries\/regions and codes, see the [Italian Revenue Agency](http://go.microsoft.com/fwlink/?LinkID=206524).  
  
### To specify the current threshold amount  
  
1.  In the **Search** box, enter **\($ N\_472 VAT Posting Setup $\)**, and then choose the related link.  
  
2.  In the **\($ N\_472 VAT Posting Setup $\)** window, on the **Navigate** tab, in the **Setup** group, choose **Blacklist Comm. Amount**.  
  
3.  In the **\($ N\_12191 Blacklist Comm. Amounts $\)** window, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_12194\_1 Start Date $\)**|Specifies the start date for the threshold amounts. Transactions that are posted on or after this date are included in the calculations for the blacklist communication report.|  
    |**\($ T\_12194\_2 Threshold Amount $\)**|Specifies the minimum invoice base amount, per document, that will be included in the blacklist communication report. This amount is determined by the requirements from the tax authorities. The date used for the threshold reporting is the end date of the Blacklist reporting period.|  
  
 For the current threshold amount, see the [Italian Revenue Agency](http://go.microsoft.com/fwlink/?LinkID=206524).  
  
### To specify a vendor as the customs authority vendor  
  
1.  In the **Search** box, enter **\($ N\_12132 Customs Authority Vendors $\)**, and then choose the related link.  
  
2.  In the **\($ T\_12122\_1 Vendor No. $\)** field, select the relevant vendor.  
  
     For more information, see [\($ N\_12132 Customs Authority Vendors $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Italy/-$-n_12132-customs-authority-vendors-$-.md) window.  
  
### To set up and view the Blacklist statement template  
  
1.  In the **Search** box, enter **\($ N\_318 VAT Statement Templates $\)**, and then choose the related link.  
  
2.  From the list, choose **Blacklist**.  
  
     The template specifies which reports and pages IDs that are used with the Blacklist Communication report. The template fields are described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_255\_1 Name $\)**|Specifies the name of the template, **Blacklist**.|  
    |**\($ T\_255\_2 Description $\)**|Specifies a description of the template, Blacklist Communication.|  
    |**\($ T\_255\_6 Form ID $\)**|Specifies the window where you set up the list of transactions for the blacklist communication, **12110**.|  
    |**\($ T\_255\_7 VAT Statement Report ID $\)**|Specifies the report that prints the list of transactions for the blacklist communication, **12128**.|  
    |**\($ T\_255\_12100 VAT Stat. Export Report ID $\)**|Specifies the report that exports the list of transactions for the blacklist communication, **12129**.|  
  
3.  Optional. Select the VAT Statement template, and on the **Navigate** tab, choose **Statement Names**. You can provide the template with a name and description. Otherwise, the template will have the name Default when you access it in the **Blacklist Communication** window.  
  
## Creating the List of Transactions  
 Depending on the size and type of company, you must generate and submit a report of transactions with vendors in blacklisted countries\/regions on a monthly or quarterly basis. A suggested mapping of transactions to [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] accounts is provided in the following procedure, based on Spesometro 2013.  
  
#### To set up the template to create the list of Blacklist transactions  
  
1.  In the **Search** box, enter **Blacklist Communication**, and then choose the related link.  
  
2.  In the **Name** field, select the relevant VAT statement name.  
  
3.  Fill in the lines with the relevant information as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]Field|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|**Data Type**|  
    |--------------------------------------|---------------------------------------|-------------------|  
    |**Row No.**|Specify a row number. To enable correct filtering, we recommend that you number rows as follows: 1001..1006, and so forth.|Code|  
    |**Description**|Enter a description of the line. You can enter up to a maximum of 50 characters.<br /><br /> The types of transactions that you are required to report include the sales and purchase of goods and services. These transactions can be taxable, non\-taxable, or exempt. Also subject to reporting are invoices for transactions that are not subject to VAT.<br /><br /> Finally, you must also include information for credit note transactions.|Text|  
    |**Type**|Specify the Type of the account that the blacklist report will include, for example, VAT Entry Totaling.|Option|  
    |**Blacklist Country\/Region Transaction**|Select the check box to include information from VAT entries that originate with a person or organization that has their residence in a blacklist country\/region. In general, only select the check box when the Type of the line is VAT Entry Totaling.<br /><br /> If the check box is not selected, [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] only retrieves non\-blacklist items.|Boolean|  
    |**Gen. Posting Type**|Select a posting type. For the blacklist communication report, you can choose any of the options, but typical choices are one of the following:<br /><br /> Sale<br /><br /> Purchase<br /><br /> If you leave the field blank, [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] will only return VAT Statement lines that have this field blank as well.<br /><br /> If you choose the Type VAT Entry Totaling, then in this field, you can only choose among Purchase, Sale, and Settlement.|Option|  
    |**EU Service**|Specify whether the entry total represents sales of services to other EU countries\/regions.|Boolean|  
    |**Document Type**|Specify a document type. You can choose any of the options, but typical choices are one of the following:<br /><br /> Invoice<br /><br /> Credit Memo<br /><br /> If you leave the field blank, then Microsoft Dynamics NAV returns all document types.|Option|  
    |**Refers To Period**|Specify what period the documents refer to. When you export data and you have not specified a date, the setting in this field is ignored.<br /><br /> If you have leave this field blank, then [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] returns those entries that have this field blank as well. In addition, it returns those entries that are without reverse sales for VAT Entry Totaling.|Option|  
    |**VAT Bus. Posting Group**|Specify a VAT Business Posting Group. Fill in this field when the Type of the line is VAT Entry Totaling.<br /><br /> If you leave this field blank, then [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] returns entries with any specified group.|Code|  
    |**VAT Prod. Posting Group**|Specify a VAT Product Posting Group. Fill in this field when the Type of the line is VAT Entry Totaling.<br /><br /> If you leave this field blank, then [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] returns entries with any specified group.|Code|  
    |**Amount Type**|Specify the type of the Amount that is being reported. Options include:<br /><br /> Base<br /><br /> Amount<br /><br /> If you leave this field blank, then [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] returns no information.|Option|  
    |**Row Totaling**|Specify which rows are to be totaled. For example, you can enter 1001..1006 to total those rows.|Text|  
    |**Round Factor**|Specify a rounding factor that is used to round the VAT entry amounts.|Option|  
    |**Calculate with**|Specify whether to calculate the amount with a sign or the opposite sign.|Option|  
    |**Print**|Specify if you want to print information from the line.|Boolean|  
    |**Print with**|Specify whether to include the sign of the amount when you print.|Option|  
    |**Blacklisted Comm. Field**|Specify the field that the VAT totaling should map to in the file to be exported. Valid entries are limited to what is defined in the Spesometro 2013: BL003001 – BL008002. **Important:**  The **Blacklisted Comm.** field can contain only the currently required field names that are specified by Spesometro. If you specify another field name, [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] displays an error message. <br /><br /> For example, specify BL005001 for the total base amount for credit notes relating to customer transactions.<br /><br /> If you leave the field blank, the field will not be exported, but it will be part of the printout that you use for review. If you map multiple [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] account fields to the same Blacklist Comm. Field value, the export of the data will be the sum of those lines. The printout will list each line.|Code|  
    |**New Page**|Specify if you want to insert a new page after the line when you print the information.|Boolean|  
  
 The printed report includes all transactions that meet threshold requirements. It does not include those transactions that do not.  
  
#### To create and print the list of transactions  
  
1.  In the **Search** box, enter **\($ N\_12110 Blacklist Communication $\)**, and then choose the related link.  
  
2.  In the **Name** field, select the relevant VAT statement name.  
  
3.  Fill in the lines with the relevant information. See the procedure for setting up the Blacklist template.  
  
4.  On the **Actions** tab, choose **Print**.  
  
5.  Optionally, on the **VAT Statement Line** FastTab, set the relevant filters.  
  
6.  On the **Options** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ R\_12128\_N\_2\_12 Starting Date $\)**|Optional. Enter the start date for the blacklist report, which is based on the date that the operations occurred.|  
    |**\($ R\_12128\_N\_2\_10 Ending Date $\)**|Enter the end date for the blacklist report.|  
    |**\($ R\_12128\_N\_2\_1 Include VAT Entries $\)**|Specify if the list of transactions must include open or closed VAT entries or both open and closed VAT entries.|  
    |**\($ R\_12128\_N\_2\_4 Include VAT Entries $\)**|Specify if the list of transactions must include VAT entries that are in the specified VAT period or must also include VAT entries that are from previous periods.|  
    |**\($ R\_12128\_N\_2\_1130006 VAT Period $\)**|Enter the time that defines the VAT period for the blacklist report.|  
    |**\($ R\_12128\_N\_2\_1130005 Source Type $\)**|Optional. Enter the source type of the blacklist transactions. The options include **Customer** and **Vendor**. If nothing is selected, both groups are included.|  
    |**\($ R\_12128\_N\_2\_1130007 Source No. $\)**|If you choose a **Source Type**, then enter the identification number of the source transaction. If nothing is entered, then all vendors or customers are included.|  
    |**\($ R\_12128\_N\_2\_1130004 Name $\)**|Read\-only. Specifies the name of the organization.|  
  
7.  Choose the **Print** button to print the report, or choose the **Preview** button to view the results.  
  
    > [!NOTE]  
    >  The printed report includes all transactions that meet threshold requirements. It does not include those transactions that do not.  
  
#### To preview and export the list of transactions  
  
1.  In the **Search** box, enter **\($ N\_12110 Blacklist Communication $\)**, and then choose the related link.  
  
2.  In the **Name** field, select the relevant VAT statement name.  
  
3.  Fill in the lines with the relevant information. See the procedure for setting up the Blacklist template.  
  
4.  On the **Navigate** tab, choose **Preview**. You can review the information to make sure that your mappings have provided you with the information that you expected. For more information, see [\($ N\_12138 Blacklisted Comm. Preview $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Italy/-$-n_12138-blacklisted-comm.-preview-$-.md) window. Choose the **OK** button to close the window  
  
5.  On the **Actions** tab, choose **Export**.  
  
6.  Optionally, on the **VAT Statement Line** FastTab, set the relevant filters.  
  
7.  On the **Options** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ R\_12129\_N\_2\_12 Starting Date $\)**|Enter the start date for the blacklist report.|  
    |**\($ R\_12129\_N\_2\_10 Ending Date $\)**|Enter the end date for the blacklist report.|  
    |**\($ R\_12129\_N\_2\_1 Include VAT Entries $\)**|Specify if the list of transactions must include open or closed VAT entries or both open and closed VAT entries.|  
    |**\($ R\_12129\_N\_2\_4 Include VAT Entries $\)**|Specify if the list of transactions must include VAT entries that are in the specified VAT period or must also include VAT entries that are from previous periods.|  
    |**\($ R\_12129\_N\_2\_1130006 VAT Period $\)**|Enter the time that defines the VAT period for the blacklist report.|  
    |**\($ R\_12129\_N\_2\_1130001 Communication Type $\)**|Enter the communication type for the blacklist export. The options include \<blank\>, **Corrective** and **Cancellation**.<br /><br /> If you enter **Corrective**, then a full report will be generated for the specified period, but you have the option to overwrite a previously submitted report.<br /><br /> If you enter **Cancellation**, then you have to provide the values from the previously generated report and a new report will be generated.<br /><br /> You enter information about the corrective or cancellation action in the **Substitution Data**  group. Fill in the following fields, using information that was that was provided by the Italian Revenue Agency \(IVA\) in its communication with you when you originally submitted your blacklist report:<br /><br /> -   **\($ B\_12129\_N\_2\_1130000 Substitution Report No. $\)**<br />-   **\($ B\_12129\_N\_2\_1130002 Substitution Doc. No. $\)**|  
    |**\($ R\_12129\_N\_2\_1130004 Period Type $\)**|Specify if the report is monthly or quarterly.|  
  
8.  Choose the **OK** button.  
  
    > [!NOTE]  
    >  The exported file includes those transactions that are above the current threshold amount.  
  
 You can now submit the list of transactions to the Italian Revenue Agency. If you have more than 1500 records, multiple files will be exported.  
  
## See Also  
 [\($ R\_12128 Blacklist Communication Report $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Italy/-$-r_12128-blacklist-communication-report-$-.md)   
 [\($ N\_12110 Blacklist Communication $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Italy/-$-n_12110-blacklist-communication-$-.md)   
 [\($ N\_12132 Customs Authority Vendors $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Italy/-$-n_12132-customs-authority-vendors-$-.md)   
 [\($ N\_472 VAT Posting Setup $\)](assetId:///a96dd9fe-bfcb-46d8-874f-1046a0dcc1f7)   
 [\($ N\_10 Countries\/Regions $\)](assetId:///bf41e72c-c814-4b75-8364-efb0136882a4)   
 [Italian VAT](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Italy/italian-vat.md)