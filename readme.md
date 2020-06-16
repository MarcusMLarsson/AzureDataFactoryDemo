<p align="center"><img src="https://www.element61.be/sites/default/files/competence/Azure%20Factory/image%201.png" width="500"> </p>

<h1> <b>Introduction to Azure Data Factory </b></h1>

<h3> What is Azure Data Factory? </h3>

<p> What is at the core of every Business Intelligence, Data Science, and Machine Learning project? <b>Data!</b> You need to collect, move, store, transform, integrate, and prepare your data. That can be a pretty time-consuming task, right? Wouldn’t it be cool if we could do all of those things automatically, like, in a data factory or something? Azure Data Factory (ADF) is a <b>cloud  ETL and data integration tool</b> that enables you to quickly and efficiently create automated data pipelines – without having to write any or little amount of code!  </p>

<h3> What can you do with Azure Data Factory? </h3>

<p> At its core, Azure Data Factory can be used to ingest and transform data. You can ingest data to and from 
<ul> <li> more than 80 Software-as-a-Service (SaaS) applications (such as Dynamics 365 and Salesforce) </li>
  <li> on-premises data stores (such as SQL Server and Oracle) </li>
  <li> and cloud data stores (such as Azure SQL Database and Amazon S3) </li>
  </ul>

During ingestion, you can even convert file formats, zip and unzip files, and map columns implicitly and explicitly – all in one task. In addition to ingesting data, you can also transform data. Previously, the only way to do this was to use external services like Azure HDInsight or SQL Server Stored Procedures. But in 2019, Azure Data Factory completed the data integration story by adding new data transformation capabilities called Data Flows. Now you can both ingest and transform data in the same user interface, making Azure Data Factory a complete ETL and data integration tool. </p>

<h3> On-premise ETL vs Cloud ETL</h3>

<b> On-premise ETL </b>
<p> For on-premise ETL solutions, SQL Server Integration Services (SSIS) is still the industry-standard. SSIS has been around since 2005. It’s very mature and has a lot of learning resources, blogs and articles as how to setup and develop with it. SSIS provides connectors to many different sources and contains many different transformation tasks that can handle pretty much any kind of traditional ETL workflow. For those people moving to Azure and who has sunk a lot of development time into SSIS, have no fear. It's very easy to lift and shift your solutions to the cloud.
<ul>
  <li> If you are looking for a PaaS-based approach, you can simply lift your SQL Server virtual machine running SSIS into the cloud. </li>
  <li> For those who want to leverage a PaaS-based approaches, Azure now offers the facility to publish your SSIS packages directly into Data Factory. </li>
</ul>
 
 <b> Cloud ETL </b> 
  
<p> It has becoming increasingly more difficult to do traditional ETL using tools like SSIS as the scale and the size of the data to be processed has grown. Azure Data Factory allows you to copy data at massive scale, and then use processing tools (e.g. Databricks) more appropriate to the job to transform the data ready for usage downstream. This pattern is not dissimilar to a common pattern seen in SSIS wherein developers used SSIS as the orchestrator and calls a series of SQL Statements (often Stored Procedures) to handle the processing. The difference now is that it’s not just relational tables we’re dealing with and SQL code. It’s parquet, orc and avro combined with SQL and Python, mixed with JSON, NoSQL, Key Value pairs and Graph databases plus a sprinkle of Spark etc. The table below, highlights some of the differences between Azure Data Factory and SSIS.

  | Azure Data Factory     | SSIS     |
| ------------- |:-------------:|
| High volumn of data | Medium volumn of data|
| Batch & Streaming | Batch    |
| Structured, Unstructured & Schema-drift | Structured       |
| Drag and Drop & Code (CLI & SDK)  | Drag and Drop       |
| C#, Python, PowerShell CLI  |  VB, C# & Biml| 
| Hybrid, Managed, Scale up  |On-Premises, Own Hardware, Scale out | 
| Pay as you go  | Licenses| 

  <h3> A deeper dive into Azure Data Factory </h3> 

  <p> Azure Data Factory consists of 6 main components. If you understand these components, you understand Azure Data Factory. The components are the following: </p>
     <img src="https://www.cathrinewilhelmsen.net/scribbles/wp-content/uploads/2019/11/CathrineWilhelmsenBeginnersGuidetoAzureDataFactory03_Components-1.png">
  
  <ul> 
  <li> <b>Pipeline </b></li>
  <p> A pipeline is a logical set of activities. The advantages of the pipeline is that it allows you to manage these activities as a set, instead of each one individually. </p>
  <li> <b>Activitites </b></li>
  <p> Activities are handeling the data. There are three types of activities in Azure Data Factory. 
    <ul>
      <li> Data movement activitites</li>
      <p> Copies and moves data from different sources </p>
      <li> Data transformation activitites</li>
      <p> You can use Data Flows (Azure Data Factory interface) or external services like Databricks, HDinsight (Hive, Hadoop, Spark, Pig, MapReduce), Azure ML etc. 
      <li> Data Control</li>
      <p> Defines the logic that your pipeline is going to follow. Its the orchestration of pipeline activities that includes chaining activities in a sequence, branching etc. </p>
  </ul>   
    <li> <b>Datasets </b></li>
  <p> Datasets represent data structures within the data stores, which simply point to or reference the data you want to use in your activities as inputs or outputs. </p>
  <li> <b>Linked services </b></li>
  <p> This is very similar to the concept of a connection string, where you are specifying what the source and destination of your data is. </p>
   <li> <b>Integration runtime </b></li>
  <p> The Integration Runtime (IR) is the compute infrastructure used by Azure Data Factory </p>
  <li> <b>Triggers </b></li>
  <p> A trigger determines when a pipeline needs to be run. </p>
  </ul>

  
  
  
  
  
  
  <h3> Demo </h3>
  
<img src="https://raw.githubusercontent.com/MarcusMLarsson/Azure-Data-Factory-Demo/master/source/image.PNG">
  
  <hr>
  
  


<h3> Cost </h3>


<p> Databricks , preperation, collaboration, AI / ML </p>



Iterative development and debugging by using visual tools




 | Azure Data Factory     | SSIS     |
| ------------- |:-------------:|
| Pipeline  | Package|
| Activity   | Task     |
| Linked Services | Connection Managers       |
| Datasets  |SSIS Sources and Destinations        |
| Source/Sink   |Source/Destination       |
| uses Json files  |uses DTSX (XML)| 








<h3> Modern Data Warehouse</h3>





<h3> Demo </h3>

<p> Introduction to ETL in Azure Data Factory. Importing csv data from Blob to Azure SQL </p>

<p>Drag wait activity</p>


<p> https://sqlofthenorth.blog/category/data-factory/ </p>
