# RD Station Power BI Report 
### Lead capture tool with Power Automate, Sharepoint and Power BI
This Power BI report queries a JSON file containing lead data, which is generated via a webhook integration between RD Station and Power Automate. The automated flow stores new leads in a Sharepoint folder, creating a dynamic and queryable database for reporting purposes.

### Context and goal
The company launched a marketing campaing for an educational course. A subscription form created using RD Station was embbeded on a landing page. Project's stakeholders needed to monitor the campaing's performance and access a centralized, shareable lead database with access control. 

### Architecture and workflow
#### Database creation
RD Station sends lead data via *webhook (push method)*, while Power BI queries data sources using a *pull method*. Therefore, an automated flow was created in *Power Automate* to receive, filter and transform webhook data. Then, the processed data is stored in a JSON file within a *Sharepoint* folder. Sharepoint was chosen as the storage layer because the company didn't provided a data warehouse or a data lake access.

This setup allows Power BI to connect and refresh the lead database whenever needed without requiring any external services or custom APIs.
