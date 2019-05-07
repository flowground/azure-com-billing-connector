# ![LOGO](logo.png) BillingManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the BillingManagementClient API (version 2018-03-01-preview).

Generated from: https://api.apis.guru/v2/specs/azure.com/billing/2018-03-01-preview/swagger.json<br/>
Generated at: 2019-05-07T17:37:40+03:00

## API Description

Billing client provides access to billing resources for Azure subscriptions.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists the enrollment accounts the caller has access to.

*Tags:* `EnrollmentAccounts`

#### Input Parameters
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.

### Gets a enrollment account by name.

*Tags:* `EnrollmentAccounts`

#### Input Parameters
* `name` - _required_ - Enrollment Account name.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.

### Lists all of the available billing REST API operations.

*Tags:* `Operations`

#### Input Parameters
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.

### Lists the available billing periods for a subscription in reverse chronological order. This is only supported for Azure Web-Direct subscriptions. Other subscription types which were not purchased directly through the Azure web portal are not supported through this preview API.

*Tags:* `BillingPeriods`

#### Input Parameters
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.
* `$filter` - _optional_ - May be used to filter billing periods by billingPeriodEndDate. The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'.
* `$skiptoken` - _optional_ - Skiptoken is only used if a previous operation returned a partial result. If a previous response contains a nextLink element, the value of the nextLink element will include a skiptoken parameter that specifies a starting point to use for subsequent calls.
* `$top` - _optional_ - May be used to limit the number of results to the most recent N billing periods.

### Gets a named billing period.  This is only supported for Azure Web-Direct subscriptions. Other subscription types which were not purchased directly through the Azure web portal are not supported through this preview API.

*Tags:* `BillingPeriods`

#### Input Parameters
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.
* `billingPeriodName` - _required_ - The name of a BillingPeriod resource.

### Lists the available invoices for a subscription in reverse chronological order beginning with the most recent invoice. In preview, invoices are available via this API only for invoice periods which end December 1, 2016 or later.  This is only supported for Azure Web-Direct subscriptions. Other subscription types which were not purchased directly through the Azure web portal are not supported through this preview API.

*Tags:* `Invoices`

#### Input Parameters
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.
* `$expand` - _optional_ - May be used to expand the downloadUrl property within a list of invoices. This enables download links to be generated for multiple invoices at once. By default, downloadURLs are not included when listing invoices.
* `$filter` - _optional_ - May be used to filter invoices by invoicePeriodEndDate. The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'.
* `$skiptoken` - _optional_ - Skiptoken is only used if a previous operation returned a partial result. If a previous response contains a nextLink element, the value of the nextLink element will include a skiptoken parameter that specifies a starting point to use for subsequent calls.
* `$top` - _optional_ - May be used to limit the number of results to the most recent N invoices.

### Gets the most recent invoice. When getting a single invoice, the downloadUrl property is expanded automatically.  This is only supported for Azure Web-Direct subscriptions. Other subscription types which were not purchased directly through the Azure web portal are not supported through this preview API.

*Tags:* `Invoices`

#### Input Parameters
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.

### Gets a named invoice resource. When getting a single invoice, the downloadUrl property is expanded automatically.  This is only supported for Azure Web-Direct subscriptions. Other subscription types which were not purchased directly through the Azure web portal are not supported through this preview API.

*Tags:* `Invoices`

#### Input Parameters
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2018-03-01-preview.
* `invoiceName` - _required_ - The name of an invoice resource.

## License

**flow**ground :- Telekom iPaaS / azure-com-billing-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
