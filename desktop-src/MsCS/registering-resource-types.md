---
title: Registering Resource Types
description: The following procedure describes how to register new resource types from a cluster-aware setup application. You should complete the steps described in Installing Files before proceeding.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: aa642609-ad7f-43fc-8189-5afeacbc0646
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- resource types Failover Cluster , registering
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Registering Resource Types

The following procedure describes how to register new [resource types](resource-types.md) from a [*cluster-aware*](https://www.bing.com/search?q=*cluster-aware*) setup application. You should complete the steps described in [Installing Files](installing-files.md) before proceeding.

1.  For each resource type supported by your [resource DLL](resource-dlls.md), call [**CreateClusterResourceType**](/previous-versions/windows/desktop/api/ClusAPI/nc-clusapi-pclusapi_create_cluster_resource_type) once from any cluster [node](nodes.md). This establishes the new resource type in the [*cluster*](https://www.bing.com/search?q=*cluster*) and allows the [Cluster service](cluster-service.md) to associate the resource type name with your resource DLL.
2.  Optional: Configure the [common properties](resource-type-common-properties.md) of your resource type with [CLUSCTL\_RESOURCE\_TYPE\_SET\_COMMON\_PROPERTIES](clusctl-resource-type-set-common-properties.md).
3.  Call the extension DLL's [**DLLRegisterCluAdminExtension**](dllregistercluadminextension.md) entry point once from any cluster node to register the extension DLL with the cluster.
4.  Perform COM registration for the extension DLL by calling [**DLLRegisterServer**](/previous-versions/windows/desktop/api/WtClusRes/) from each cluster node and on each remote system with a copy of the extension.

 

 



