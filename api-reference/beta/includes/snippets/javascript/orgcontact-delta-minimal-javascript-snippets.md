---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/contacts/delta')
	.version('beta')
	.header('Prefer','return=minimal')
	.select('displayName,jobTitle,mail')
	.get();

```