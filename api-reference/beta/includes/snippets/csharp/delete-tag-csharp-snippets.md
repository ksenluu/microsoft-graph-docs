---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

await graphClient.Compliance.Ediscovery.Cases["{case-id}"].Tags["{tag-id}"].DeleteAsync((requestConfiguration) =>
{
	requestConfiguration.QueryParameters.Forcedelete = true;
});


```