# CassandraAPICosmosDBHandsDirty

**Summary:**
This document provides guidance on getting your hands dirty using Azure Cosmos DB API for Cassandra Database.

## Introduction
Azure Cosmos DB Cassandra API can be used as the data store for apps written for [Apache Cassandra](https://cassandra.apache.org/_/index.html). This means that by using existing Apache drivers compliant with CQLv4, your existing Cassandra application can now communicate with the Azure Cosmos DB Cassandra API. In many cases, you can switch from using Apache Cassandra to using Azure Cosmos DB's Cassandra API, by just changing a connection string.

The Cassandra API enables you to interact with data stored in Azure Cosmos DB using the Cassandra Query Language (CQL) , Cassandra-based tools (like cqlsh) and Cassandra client drivers that you're already familiar with. For more information, visit the official Microsoft [documentation for Azure Cosmos DB API for Cassandra Database](https://docs.microsoft.com/en-us/azure/cosmos-db/cassandra/cassandra-introduction).

## About Azure Cosmos DB
Azure Cosmos DB is a fully managed NoSQL database for modern app development, with SLA-backed speed and availability, automatic and instant scalability, and open-source APIs for MongoDB, Cassandra, and other NoSQL engines. For a more in-depth coverage of Azure Cosmos DB, you should visit the official site here > https://docs.microsoft.com/en-us/azure/cosmos-db/introduction

![Image1](media/azure-cosmos-db.png)

## Getting Started
If you're looking to get started quickly, you can find a range of SDK Support and sample Tutorials using .NET, .NET Core, Java, Python etc. [here](https://docs.microsoft.com/en-us/azure/cosmos-db/cassandra/manage-data-dotnet).

## What you learn from this Sample?
Key learning include:
- Creating an Apache Cassandra Keyspace in Azure Cosmos DB using API for Cassandra leveraging C#.
- Providing provisioned throughput (RU) at keyspace level.
- Creating an Apache Cassandra Table in Azure Cosmos DB using API for Cassandra.
- Providing provisioned throughtput (RU) at table level.
- Best practices for creating a Primary Key in Cassandra (which includes 1 partitionKey + 0 or more Clustering Columns.
- Creating a table with a single Primary Key.
- Creating a table with a *Compound* Primary Key for a use-case wherein a single Primary Key will not work.
- Inserting data into both tables: uprofile.user and weather.data.
- Basic Query operations using a Basic query
- Query Operation trying to query table by filtering by non-primary key. Flags an error which is as per Cassandra Database.
- Solution to problem of querying table by filtering by non-primary key by creating a 'Secondary Index'.

## Running this Sample
This sample is in .NET. For running this sample, all you need to do is to download the Visual Studio Solution file; and then make the following changes as mentioned below. You can also leverage this GitHub repo for getting up and running quickly > https://github.com/Azure-Samples/azure-cosmos-db-cassandra-dotnet-core-getting-started.

## What you need for this Sample?
You need the following:
- An Azure subscription. If you do not have one, you can get a *free* one [here](https://azure.microsoft.com/en-in/free/) with USD 200 Credit.
- Working Azure Cosmos DB Account with Cassandra API. Learn how to create one using Azure portal [here](https://docs.microsoft.com/en-us/azure/cosmos-db/cassandra/manage-data-dotnet) using this Tutorial.
- Visual Studio Code / Visual Studio 2019 or similar IDE. You can download your VS [here](https://visualstudio.microsoft.com/downloads/).
- Working knowledge of both Apache Cassandra contructs, queries & limitations.
- Working knowledge of programming in .NET.
It is assumed that you possess all these for enjoying and doing further R&D on this sample. Simply clone this git repo (or download as Zip).

## A few things to do before deep-dive:
1. Open the Visual Studio Solution file; ensure your Nuget packages are upto date. Specifically, ensure that '[CassandraCSharpDriver](https://www.nuget.org/packages/CassandraCSharpDriver/)' is installed. Your packages.config file should resemble the same as shown below:
![Image2](media/packagesconfig.png)

2.In the Program.cs file, edit the secion below. You will find these from your Azure portal, Cosmos DB account's Settings > Connection String:
![Image3](media/image1.png)

```
// Cassandra Cluster configs section.
private const string UserName = "<< ENTER YOUR USERNAME >>"; 
private const string Password = "<< ENTER YOUR PRIMARY PASSWORD >>";
private const string CassandraContactPoint = "<< ENTER YOUR CONTACT POINT >>";  // DnsName
private static int CassandraPort = 10350;                                       // Leave this as it is
```

## Output in VS:
 
 
 
## Validate in Azure Portal:
 
 
 
