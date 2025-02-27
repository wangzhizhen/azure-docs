---
title: Solution building for Azure IoT Central | Microsoft Docs
description: Azure IoT Central is an IoT application platform that simplifies the creation of IoT solutions. This article provides an overview of building integrated solutions with IoT Central.
author: dominicbetts
ms.author: dobett
ms.date: 02/11/2021
ms.topic: conceptual
ms.service: iot-central
services: iot-central
ms.custom: mvc

# This article applies to solution builders.
---

# IoT Central solution builder guide

An IoT Central application lets you monitor and manage millions of devices throughout their life cycle. This guide is for solution builders who use IoT Central to build integrated solutions. An IoT Central application lets you manage devices, analyze device telemetry, and integrate with other back-end services.

A solution builder:

- Configures dashboards and views in the IoT Central web UI.
- Uses the built-in rules and analytics tools to derive business insights from the connected devices.
- Uses the data export and rules capabilities to integrate IoT Central with other back-end services.

## Configure dashboards and views

An IoT Central application can have one or more dashboards that operators use to view and interact with the application. As a solution builder, you can customize the default dashboard and create specialized dashboards:

- To view some examples of customized dashboards, see [Industry focused templates](concepts-app-templates.md#industry-focused-templates).
- To learn more about dashboards, see [Create and manage multiple dashboards](howto-manage-dashboards.md) and [Configure the application dashboard](howto-manage-dashboards.md).

When a device connects to an IoT Central, the device is associated with a device template for the device type. A device template has customizable views that an operator uses to manage individual devices. As a solution developer, you can create and customize the available views for a device type. To learn more, see [Add views](howto-set-up-template.md#views).

## Use built-in rules and analytics

A solution developer can add rules to an IoT Central application that run customizable actions. Rules evaluate conditions, based on data coming from a device, to determine when to run an action. To learn more about rules, see:

- [Tutorial: Create a rule and set up notifications in your Azure IoT Central application](tutorial-create-telemetry-rules.md)
- [Configure rules](howto-configure-rules.md)

IoT Central has built-in analytics capabilities that an operator can use to analyze the data flowing from the connected devices. To learn more, see [How to use analytics to analyze device data](howto-create-analytics.md).

## Integrate with other services

As a solution builder, you can use the data export and rules capabilities in IoT Central to integrate with other service. To learn more, see:

- [Export IoT data to cloud destinations using data export](howto-export-data.md)
- [Transform data for IoT Central](howto-transform-data.md)
- [Use workflows to integrate your Azure IoT Central application with other cloud services](howto-configure-rules-advanced.md)
- [Extend Azure IoT Central with custom rules using Stream Analytics, Azure Functions, and SendGrid](howto-create-custom-rules.md)
- [Extend Azure IoT Central with custom analytics using Azure Databricks](howto-create-custom-analytics.md)

You can use IoT Edge devices connected to your IoT Central application to integrate with [Azure Video Analyzer](../../azure-video-analyzer/video-analyzer-docs/overview.md). To learn more, see the [Azure IoT Central gateway module for Azure Video Analyzer](https://github.com/iot-for-all/iotc-ava-gateway/blob/main/README.md) on GitHub.

## APIs

IoT Central APIs let you build deep integrations with other services in your IoT solution. The available APIs are categorized as *data plane* or *control plane* APIs.

You use data plane APIs to access the entities in and the capabilities of your IoT Central application. For example managing devices, device templates, users, and roles. The IoT Central REST API operations are *data plane* operations. To learn more, see [How to use the IoT Central REST API to manage users and roles](howto-manage-users-roles-with-rest-api.md).

You use the *control plane* to manage IoT Central-related resources in your Azure subscription. You can use the Azure CLI and Resource Manager templates for control plane operations. For example, you can use the Azure CLI to create an IoT Central application. To learn more, see [Manage IoT Central from Azure CLI](howto-manage-iot-central-from-cli.md).

## Transform data at ingress

Devices may send complex telemetry that needs to be simplified before it's used in IoT Central or exported. In some scenarios you need to normalize the telemetry from different devices so that you can display and process the telemetry consistently. To learn more, see [Map telemetry on ingress to IoT Central](howto-map-data.md).

## Next steps

If you want to learn more about using IoT Central, the suggested next steps are to try the quickstarts, beginning with [Create an Azure IoT Central application](./quick-deploy-iot-central.md).
