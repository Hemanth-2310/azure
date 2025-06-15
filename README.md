Cost Optimization for Billing Records in Azure Cosmos DB
The core problem is the increasing cost of Cosmos DB due to a large volume of infrequently accessed, old data. The solution needs to move this cold data to a cheaper storage tier while maintaining accessibility and adhering to existing API contracts, with no downtime or data loss.


Proposed Solution: Tiered Storage with Azure Data Lake Storage Gen2
The most efficient and straightforward approach is to implement a tiered storage strategy. We will leverage Azure Data Lake Storage Gen2 (ADLS Gen2) for archival storage due to its cost-effectiveness for large volumes of data and its hierarchical namespace capabilities, which make data organization and retrieval efficient. Azure Functions will orchestrate the data movement, and a "hot/cold" data access pattern will be implemented.
