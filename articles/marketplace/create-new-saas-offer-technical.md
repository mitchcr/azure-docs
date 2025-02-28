---
title: Add technical details for a SaaS offer in Azure Marketplace
description: Provide technical details for a software as a service (SaaS) offer in Azure Marketplace. 
author: mingshen-ms
ms.author: mingshen
ms.service: marketplace 
ms.subservice: partnercenter-marketplace-publisher
ms.topic: how-to
ms.date: 10/25/2021
---

# Add technical details for a SaaS offer

This article describes how to enter technical details that help the Microsoft commercial marketplace connect to your solution. This connection enables us to provision your offer for the customer if they choose to acquire and manage it. For more details about these settings, see [Technical information](plan-saas-offer.md#technical-information).

> [!NOTE]
> If you choose to process transactions independently, you will not see this option. Instead, skip to [How to sell your SaaS offer](create-new-saas-offer-marketing.md).

## Technical configuration

On the **Technical configuration** tab, you'll define the technical details that the commercial marketplace uses to communicate to your SaaS application or solution.

- **Landing page URL** (required) – Define the SaaS website URL (for example: `https://contoso.com/signup`) that customers will land on after acquiring your offer from the commercial marketplace and triggering the configuration process from the newly created SaaS subscription.

  > [!IMPORTANT]
  > Your landing page should be up and running 24/7. This is the only way you will be notified about new purchases of your SaaS offers made in the commercial marketplace, or configuration requests of an active subscription of an offer. Don't include the pound sign character (#) in the landing page URL. Otherwise, customers will not be able to access your landing page.

- **Connection webhook** (required) – For all asynchronous events that Microsoft needs to send to you (for example, SaaS subscription has been canceled), we require you to [provide a connection webhook URL](./partner-center-portal/pc-saas-fulfillment-webhook.md). We will call this URL to notify you of the event.

  > [!IMPORTANT]
  > Your webhook should be up and running 24/7 as this is the only way you will be notified about updates about your customers' SaaS subscriptions that are purchased via the commercial marketplace.

- **Azure Active Directory tenant ID** (required) – To find the tenant ID for your Azure Active Directory (Azure AD) app, go to the [App registrations](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) blade in Azure Active Directory. In the **Display name** column, select the app. Then look for the **Directory (tenant) ID** number listed (for example, `50c464d3-4930-494c-963c-1e951d15360e`).

- **Azure Active Directory application ID** (required) – To find your [application ID](../active-directory/develop/howto-create-service-principal-portal.md#sign-in-to-the-application), go to the [App registrations](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) blade in Azure Active Directory. In the **Display name** column, select the app. Then look for the Application (client) ID number listed (for example, `50c464d3-4930-494c-963c-1e951d15360e`).

Select **Save draft** before continuing to the next tab: Plan overview.

## Next steps

- [Create plans for a SaaS offer](create-new-saas-offer-plans.md).
