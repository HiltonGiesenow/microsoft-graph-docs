---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String use = "sig";

String kty = "RSA";

int nbf = 1508969811;

int exp = 1508969811;

graphClient.trustFramework().keySets("{id}")
	.generateKey(use,kty,nbf,exp)
	.buildRequest()
	.post();

```