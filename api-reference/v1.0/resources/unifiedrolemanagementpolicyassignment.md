---
title: "unifiedRoleManagementPolicyAssignment resource type"
description: "The assignment of a role management policy to a role definition object."
author: "rkarim-ms"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: resourcePageType
---

# unifiedRoleManagementPolicyAssignment resource type

Namespace: microsoft.graph

The assignment of a role management policy to a [role definition](../resources/unifiedroledefinition.md) object.

Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List unifiedRoleManagementPolicyAssignments](../api/policyroot-list-rolemanagementpolicyassignments.md)|[unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md) collection|Get a list of the [unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md) objects and their properties.|
|[Get unifiedRoleManagementPolicyAssignment](../api/unifiedrolemanagementpolicyassignment-get.md)|[unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md)|Read the properties and relationships of an [unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md) object.|

<!--
|[Create unifiedRoleManagementPolicyAssignment](../api/policyroot-post-rolemanagementpolicyassignments.md)|[unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md)|Create a new [unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md) object.|
|[Update unifiedRoleManagementPolicyAssignment](../api/unifiedrolemanagementpolicyassignment-update.md)|[unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md)|Update the properties of an [unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md) object.|
|[Delete unifiedRoleManagementPolicyAssignment](../api/unifiedrolemanagementpolicyassignment-delete.md)|None|Deletes an [unifiedRoleManagementPolicyAssignment](../resources/unifiedrolemanagementpolicyassignment.md) object.|
|[List unifiedRoleManagementPolicy](../api/unifiedrolemanagementpolicyassignment-list-policy.md)|[unifiedRoleManagementPolicy](../resources/unifiedrolemanagementpolicy.md) collection|Get the unifiedRoleManagementPolicy resources from the policy navigation property.|
|[Add unifiedRoleManagementPolicy](../api/unifiedrolemanagementpolicyassignment-post-policy.md)|[unifiedRoleManagementPolicy](../resources/unifiedrolemanagementpolicy.md)|Add policy by posting to the policy collection.|
-->

## Properties

|Property|Type|Description|
|:---|:---|:---|
|id|String|Unique identifier for the policy assignment. The ID is typically a concatenation of the **unifiedRoleManagementPolicy** ID and the **roleDefinitionId** separated by an underscore.|
|policyId|String|The id of the policy. Inherited from [entity](../resources/entity.md).|
|roleDefinitionId|String|The identifier of the [role definition](unifiedroledefinition.md) object where the policy applies. If not specified, the policy applies to all roles. Supports $filter (`eq`).|
|scopeId|String|The identifier of the scope where the policy is assigned.  Can be `/` for the tenant or a group ID. Required.|
|scopeType|String|The type of the scope where the policy is assigned. One of `Directory`, `DirectoryRole`. Required.|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|policy|[unifiedRoleManagementPolicy](../resources/unifiedrolemanagementpolicy.md)| The policy that's associated with a policy assignment. Supports `$expand` and a nested `$expand` of the **rules** and **effectiveRules** relationships for the policy.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.unifiedRoleManagementPolicyAssignment",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.unifiedRoleManagementPolicyAssignment",
  "id": "String (identifier)",
  "policyId": "String",
  "scopeId": "String",
  "scopeType": "String",
  "roleDefinitionId": "String"
}
```

