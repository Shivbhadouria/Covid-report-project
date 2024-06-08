welcome.
Now that we understand the project requirements,let's look at the architecture for our solution. As we discussed, we'll ingest the COVID-19 data
from the European Center for Disease Prevention and Control website. Otherwise called ECDC. We use the HTTP connector within Azure Data Factory to get the data.
For the Eurostat data, we'll keep the population file in an Azure storage account and ingest from there. We could get this data directly from the Eurostat website,
but we'll instead ingest from an Azure storage account.
This is only because I want to teach you
another type of connector other than HTTP connector
that we've already used for the COVID 19 data.
Both data sets will be ingested
into the Azure Data Lake storage.
We'll then use Azure Data Factory to transform this data.
We'll use the transformation capability
called Data Flows within the Data Factory
for the couple of data sets.
We'll use HDInsight for another data set
and Azure data bricks for another one.
For the HDInsight and the data bricks transformations,
Data Factory will be used
as the orchestration tool
rather than the transformation tool.
All of the transformed data
will then be stored in our Data Lake
for use in machine learning models.
We won't be building the machine learning models
as it's out scope for this course.
We'll also push the subset of the required data
to the SQL database so that it can be used for reporting.
We'll then build a Power BI report from this data.
The focus of this course is
Azure Data Factory rather than Power BI.
But I'll do a quick lesson on building the report.
Let's now have a look at the solution
to understand why we've used these specific technologies.
Firstly, we've used Azure Data Factory
for all our data integration and orchestration.
We used ADF for data integration
because it provides connectors
to all our data sources in this project.
And also it provides a vast array of connectors
that could be used to expand the project
in the future when a new requirement arises.
Similarly, Data Factory has the connectors
to orchestrate our workflow.
For example, it can orchestrate the workflow
with running transformations
in HDInsight and Azure databricks.
Next, let's have a look
at the transformation technologies being used.
We've used three transformation technologies here,
Data Flow within Data Factory, HDInsight,
and Azure Databricks.
I'm using all three just to show you the capabilities
of Azure Data Factory.
We can use any one of these to meet all our needs
in this project,
but I just wanted to show you
and make you understand the differences
so that you can use the right one in your projects.
All three of these technologies
are run on distributed infrastructure
and they're easily scalable.
The difference is that
Data Flow gives you a code free transformation tool
which makes it easy to develop
and maintain the transformation.
But at the same time,
it is good
for simple and medium level complexity transformations,
but it lacks in its ability
to develop complex transformations.
The other two options,
HDInsight and Databricks,
will require you to write the code
in one of Spark supported languages
such as Python, Scholar or Spark SQL.
HDInsight also gives you the ability to write code
in a SQL like language called Hive
and also a scripting language called Pig.
So based on this,
you should choose the tool of your choice
depending on your requirement
and the technical skill available within the team.
Now let's have a look at the storage solutions used.
We're using Azure Blob storage to keep the population data,
Azure Data Lake storage Gen 2 as the Data Lake,
Azure SQL database for our data warehouse solution
let's go through each one of these.
Azure Blob storage is a solution
for storing large amount of text or binary data.
You can use Blob storage
to distribute data centrally in a business
or to expose to the world.
In this case,
let's assume that one of our teams
have collected data from Eurostat
about the country's population information,
curated the data
and made it available for other business areas.
And we are one of the teams
for which the data has been distributed
via the Blob storage.
Next, we've used as Azure Data Lake Gen 2
for our Data Lake.
Azure Data Lake Gen 2
is Azure's recommended storage solution
for building enterprise level Data Lakes.
It can store multiple petabytes of data
while sustaining hundreds of gigabytes of throughput.
This is built on top of Azure Blob storage
so it is cost effective, but with it add a benefits
of better performance management and security.
You can mount Data Lake storage
to add the big data solutions
such as Hadoop databases and synapse analytics.
And finally, we've used Azure's SQL database
for our data warehouse solution.
Azure's synapse analytics
formally called Azure data warehouse,
is a better solution
for large data warehouses
due to its massively parallel processing architecture.
We're using SQL database instead.
Mainly due to the small amount of data we are processing.
If you would like to use Synapse, please feel free to do so.
Everything taught here should work
except for connectors to the database
which you'll have to point at the synapse connectors
rather than the SQL database connections.
We using Power BI to report the trends we want to report.
it has rich features that we can use
to develop meaningful reports and share across our teams.
Hope this has given you an understanding
of our solution architecture.
In the future lessons,
I'll give you more insights
into everything that we've discussed here.
So that's the end of this lesson
and I'll see in the next one.




