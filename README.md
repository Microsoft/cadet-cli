# cadet-cli

[![Build Status](https://dev.azure.com/csebostoncrew/Cadet-CLI/_apis/build/status/Microsoft.cadet-cli?branchName=master)](https://dev.azure.com/csebostoncrew/Cadet-CLI/_build/latest?definitionId=26?branchName=master)

**C**osmos **A**utomated **D**ata **E**xchange **T**ool - A cross-platform utility to synchronize data with a [DocumentDB](https://docs.microsoft.com/en-us/azure/cosmos-db/create-sql-api-dotnet)-backed [Azure Cosmos DB](https://azure.microsoft.com/en-us/services/cosmos-db/) instance. 👩‍🚀☁

![Cadet-cli branded logo of a rocketship](./.github/logo.png)

You can __install the latest version of `cadet` from the [Releases](https://github.com/Microsoft/cadet-cli/releases/latest) page__, right here on GitHub.

## How it works

> Note: at this time, `cadet` [does not support](https://github.com/Microsoft/cadet-cli/issues/1) downloading data from Azure Cosmos DB.

Cadet is designed to make it simple to exchange data with Azure Cosmos DB instances that are using the [DocumentDB](https://docs.microsoft.com/en-us/azure/cosmos-db/create-sql-api-dotnet) backing store. It is a cross-platform [python](https://www.python.org/) CLI that leverages the Azure Cosmos DB python SDK under the hood. Here are some common things you can do using `cadet`:

### Import data from csv

The following command will import a comma-separated values file into the Azure Cosmos DB server located at `your-server-connection-string` into the collection `your-collection-name` on database `your-database-name`. It will read the data from `path/to/csv.csv`, and will output progress as data uploads.

```
cadet import --type csv --connection-string "your-server-connection-string" --database "your-database-name" --collection "your-collection-name" path/to/csv.csv
```

### Import data from tsv

The following command will import a tab-separated values file into the Azure Cosmos DB server located at `your-server-connection-string` into the collection `your-collection-name` on database `your-database-name`. It will read the data from `path/to/tsv.tsv`, and will output progress as data uploads.

```
cadet import --type tsv --connection-string "your-server-connection-string" --database "your-database-name" --collection "your-collection-name" path/to/tsv.tsv
```

## Contributing

For more information - including how to get started - see the [CONTRIBUTING](./CONTRIBUTING.md) document.

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
