---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

AccessPackageAssignmentPolicy accessPackageAssignmentPolicy = new AccessPackageAssignmentPolicy();
accessPackageAssignmentPolicy.id = "b2eba9a1-b357-42ee-83a8-336522ed6cbf";
accessPackageAssignmentPolicy.accessPackageId = "1b153a13-76da-4d07-9afa-c6c2b1f2e824";
accessPackageAssignmentPolicy.displayName = "All Users";
accessPackageAssignmentPolicy.description = "All users can request for access to the directory.";
accessPackageAssignmentPolicy.isDenyPolicy = false;
accessPackageAssignmentPolicy.canExtend = false;
accessPackageAssignmentPolicy.durationInDays = 365;
RequestorSettings requestorSettings = new RequestorSettings();
requestorSettings.scopeType = "AllExistingDirectorySubjects";
requestorSettings.acceptRequests = true;
LinkedList<String> allowedRequestorsList = new LinkedList<String>();
requestorSettings.allowedRequestors = allowedRequestorsList;
accessPackageAssignmentPolicy.requestorSettings = requestorSettings;
ApprovalSettings requestApprovalSettings = new ApprovalSettings();
requestApprovalSettings.isApprovalRequired = false;
requestApprovalSettings.isApprovalRequiredForExtension = false;
requestApprovalSettings.isRequestorJustificationRequired = false;
requestApprovalSettings.approvalMode = "NoApproval";
LinkedList<String> approvalStagesList = new LinkedList<String>();
requestApprovalSettings.approvalStages = approvalStagesList;
accessPackageAssignmentPolicy.requestApprovalSettings = requestApprovalSettings;
accessPackageAssignmentPolicy.accessReviewSettings = null;

graphClient.identityGovernance().entitlementManagement().accessPackageAssignmentPolicies("b2eba9a1-b357-42ee-83a8-336522ed6cbf")
	.buildRequest()
	.put(accessPackageAssignmentPolicy);

```