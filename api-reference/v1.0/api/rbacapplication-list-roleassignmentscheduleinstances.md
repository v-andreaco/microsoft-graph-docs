---
title: "List roleAssignmentScheduleInstances"
description: "Get the instances of active role assignments in your tenant."
author: "rkarim-ms"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: apiPageType
---

# List roleAssignmentScheduleInstances
Namespace: microsoft.graph

Get the instances of active role assignments in your tenant. The active assignments include those made through [assignments and activation requests](rbacapplication-post-roleassignmentschedulerequests.md), and directly through the [role assignments API](../resources/unifiedroleassignment.md).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|RoleAssignmentSchedule.Read.Directory, RoleManagement.Read.Directory, RoleManagement.Read.All, RoleAssignmentSchedule.ReadWrite.Directory, RoleManagement.ReadWrite.Directory|
|Delegated (personal Microsoft account)|Not supported|
|Application|RoleManagement.Read.All, RoleManagement.Read.Directory, RoleManagement.ReadWrite.Directory|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /roleManagement/directory/roleAssignmentScheduleInstances
```

## Optional query parameters

This method supports the `$select`, `$filter`, and `$expand` OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [unifiedRoleAssignmentScheduleInstance](../resources/unifiedroleassignmentscheduleinstance.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_unifiedroleassignmentscheduleinstance"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/roleManagement/directory/roleAssignmentScheduleInstances
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.unifiedRoleAssignmentScheduleInstance)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#roleManagement/directory/roleAssignmentScheduleInstances",
    "value": [
        {
            "id": "lAPpYvVpN0KRkAEhdxReEAWz5Gtet_xOv8wxvTtTpfg-1",
            "principalId": "6be4b305-b75e-4efc-bfcc-31bd3b53a5f8",
            "roleDefinitionId": "62e90394-69f5-4237-9190-012177145e10",
            "directoryScopeId": "/",
            "appScopeId": null,
            "startDateTime": null,
            "endDateTime": null,
            "assignmentType": "Assigned",
            "memberType": "Direct",
            "roleAssignmentOriginId": "lAPpYvVpN0KRkAEhdxReEAWz5Gtet_xOv8wxvTtTpfg-1",
            "roleAssignmentScheduleId": "lAPpYvVpN0KRkAEhdxReEAWz5Gtet_xOv8wxvTtTpfg-1"
        },
        {
            "id": "lAPpYvVpN0KRkAEhdxReEBLS8lac5ONCgpgBiOW-8JQ-1",
            "principalId": "56f2d212-e49c-42e3-8298-0188e5bef094",
            "roleDefinitionId": "62e90394-69f5-4237-9190-012177145e10",
            "directoryScopeId": "/",
            "appScopeId": null,
            "startDateTime": null,
            "endDateTime": null,
            "assignmentType": "Assigned",
            "memberType": "Direct",
            "roleAssignmentOriginId": "lAPpYvVpN0KRkAEhdxReEBLS8lac5ONCgpgBiOW-8JQ-1",
            "roleAssignmentScheduleId": "lAPpYvVpN0KRkAEhdxReEBLS8lac5ONCgpgBiOW-8JQ-1"
        }
    ]
}
```

