---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String use = "use-value";

String k = "application-secret-to-be-uploaded";

int nbf = 1508969811;

int exp = 1508973711;

graphClient.trustFramework().keySets("{id}")
	.uploadSecret(use,k,nbf,exp)
	.buildRequest()
	.post();

```