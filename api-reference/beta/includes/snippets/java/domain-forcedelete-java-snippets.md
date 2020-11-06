---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

boolean disableUserAccounts = true;

graphClient.domains("contoso.com")
	.forceDelete(disableUserAccounts)
	.buildRequest()
	.post();

```