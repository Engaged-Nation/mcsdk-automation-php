# 
Marketing Cloud's REST API is our newest API. It supports multi-channel use cases, is much more lightweight and easy to use than our SOAP API, and is getting more comprehensive with every release.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 7.3 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/sfadincescu/mcsdk-automation-php.git"
    }
  ],
  "require": {
    "sfadincescu/mcsdk-automation-php": 1.0.0"
  }
}
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

### Usage scenarios
#### Basic usage
```php

$client = new \Api\Client();
$assetApi = $client->getAssetApi();

$asset = new SalesForce\MarketingCloud\Model\Asset();

try {
    $result = $assetApi->createAsset($asset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetApi->createAsset: ', $e->getMessage(), PHP_EOL;
}
```

Please *note* that the configuration in this scenario is taken from the environment variables.

*Environment variables:*
SFMC_ACCOUNT_ID
SFMC_AUTH_BASE_URL  (this is the urlAuthorize below)
SFMC_CLIENT_ID
SFMC_CLIENT_SECRET
SFMC_COUNTRY_CODE   (eg: US)
SFMC_KEYWORD        (SMS keyword)
SFMC_SHORT_CODE     (SMS short code)

#### Setting the configuration from code using the configuration builder
```php
use Symfony\Component\DependencyInjection\ContainerBuilder;

$client = new \Api\Client(null, null, false);

$config = $client->getConfig();
$config->setAccountId('accountId')
    ->setClientId('clientId')
    ->setClientSecret('clientSecret')
    ->setAuthBaseUrl('Set it the same as urlAccessToken')
    ->setAccessTokenUrl('Authorization URL')
    ->setResourceOwnerDetailsUrl('');

$assetApi = $client->getAssetApi();
$asset = new SalesForce\MarketingCloud\Model\Asset();

try {
    $result = $assetApi->createAsset($asset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AssetApi->createAsset: ', $e->getMessage(), PHP_EOL;
}
```

## Documentation for API Endpoints

All URIs are relative to *https://www.exacttargetapis.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AssetApi* | [**createAsset**](docs/Api/AssetApi.md#createasset) | **POST** /asset/v1/content/assets | createAsset
*AssetApi* | [**deleteAssetById**](docs/Api/AssetApi.md#deleteassetbyid) | **DELETE** /asset/v1/content/assets/{id} | deleteAssetById
*AssetApi* | [**getAssetById**](docs/Api/AssetApi.md#getassetbyid) | **GET** /asset/v1/content/assets/{id} | getAssetById
*AssetApi* | [**partiallyUpdateAssetById**](docs/Api/AssetApi.md#partiallyupdateassetbyid) | **PATCH** /asset/v1/content/assets/{id} | partiallyUpdateAssetById
*CampaignApi* | [**createCampaign**](docs/Api/CampaignApi.md#createcampaign) | **POST** /hub/v1/campaigns | createCampaign
*CampaignApi* | [**deleteCampaignById**](docs/Api/CampaignApi.md#deletecampaignbyid) | **DELETE** /hub/v1/campaigns/{id} | deleteCampaignById
*CampaignApi* | [**getCampaignById**](docs/Api/CampaignApi.md#getcampaignbyid) | **GET** /hub/v1/campaigns/{id} | getCampaignById
*TransactionalMessagingApi* | [**createEmailDefinition**](docs/Api/TransactionalMessagingApi.md#createemaildefinition) | **POST** /messaging/v1/email/definitions/ | createEmailDefinition
*TransactionalMessagingApi* | [**createSmsDefinition**](docs/Api/TransactionalMessagingApi.md#createsmsdefinition) | **POST** /messaging/v1/sms/definitions | createSmsDefinition
*TransactionalMessagingApi* | [**deleteEmailDefinition**](docs/Api/TransactionalMessagingApi.md#deleteemaildefinition) | **DELETE** /messaging/v1/email/definitions/{definitionKey} | deleteEmailDefinition
*TransactionalMessagingApi* | [**deleteQueuedMessagesForEmailDefinition**](docs/Api/TransactionalMessagingApi.md#deletequeuedmessagesforemaildefinition) | **DELETE** /messaging/v1/email/definitions/{definitionKey}/queue | deleteQueuedMessagesForEmailDefinition
*TransactionalMessagingApi* | [**deleteQueuedMessagesForSmsDefinition**](docs/Api/TransactionalMessagingApi.md#deletequeuedmessagesforsmsdefinition) | **DELETE** /messaging/v1/sms/definitions/{definitionKey}/queue | deleteQueuedMessagesForSmsDefinition
*TransactionalMessagingApi* | [**deleteSmsDefinition**](docs/Api/TransactionalMessagingApi.md#deletesmsdefinition) | **DELETE** /messaging/v1/sms/definitions/{definitionKey} | deleteSmsDefinition
*TransactionalMessagingApi* | [**getEmailDefinition**](docs/Api/TransactionalMessagingApi.md#getemaildefinition) | **GET** /messaging/v1/email/definitions/{definitionKey} | getEmailDefinition
*TransactionalMessagingApi* | [**getEmailDefinitions**](docs/Api/TransactionalMessagingApi.md#getemaildefinitions) | **GET** /messaging/v1/email/definitions/ | getEmailDefinitions
*TransactionalMessagingApi* | [**getEmailSendStatusForRecipient**](docs/Api/TransactionalMessagingApi.md#getemailsendstatusforrecipient) | **GET** /messaging/v1/email/messages/{messageKey} | getEmailSendStatusForRecipient
*TransactionalMessagingApi* | [**getEmailsNotSentToRecipients**](docs/Api/TransactionalMessagingApi.md#getemailsnotsenttorecipients) | **GET** /messaging/v1/email/messages/ | getEmailsNotSentToRecipients
*TransactionalMessagingApi* | [**getQueueMetricsForEmailDefinition**](docs/Api/TransactionalMessagingApi.md#getqueuemetricsforemaildefinition) | **GET** /messaging/v1/email/definitions/{definitionKey}/queue | getQueueMetricsForEmailDefinition
*TransactionalMessagingApi* | [**getQueueMetricsForSmsDefinition**](docs/Api/TransactionalMessagingApi.md#getqueuemetricsforsmsdefinition) | **GET** /messaging/v1/sms/definitions/{definitionKey}/queue | getQueueMetricsForSmsDefinition
*TransactionalMessagingApi* | [**getSMSsNotSentToRecipients**](docs/Api/TransactionalMessagingApi.md#getsmssnotsenttorecipients) | **GET** /messaging/v1/sms/messages/ | getSMSsNotSentToRecipients
*TransactionalMessagingApi* | [**getSmsDefinition**](docs/Api/TransactionalMessagingApi.md#getsmsdefinition) | **GET** /messaging/v1/sms/definitions/{definitionKey} | getSmsDefinition
*TransactionalMessagingApi* | [**getSmsDefinitions**](docs/Api/TransactionalMessagingApi.md#getsmsdefinitions) | **GET** /messaging/v1/sms/definitions | getSmsDefinitions
*TransactionalMessagingApi* | [**getSmsSendStatusForRecipient**](docs/Api/TransactionalMessagingApi.md#getsmssendstatusforrecipient) | **GET** /messaging/v1/sms/messages/{messageKey} | getSmsSendStatusForRecipient
*TransactionalMessagingApi* | [**partiallyUpdateEmailDefinition**](docs/Api/TransactionalMessagingApi.md#partiallyupdateemaildefinition) | **PATCH** /messaging/v1/email/definitions/{definitionKey} | partiallyUpdateEmailDefinition
*TransactionalMessagingApi* | [**partiallyUpdateSmsDefinition**](docs/Api/TransactionalMessagingApi.md#partiallyupdatesmsdefinition) | **PATCH** /messaging/v1/sms/definitions/{definitionKey} | partiallyUpdateSmsDefinition
*TransactionalMessagingApi* | [**sendEmailToMultipleRecipients**](docs/Api/TransactionalMessagingApi.md#sendemailtomultiplerecipients) | **POST** /messaging/v1/email/messages/ | sendEmailToMultipleRecipients
*TransactionalMessagingApi* | [**sendEmailToSingleRecipient**](docs/Api/TransactionalMessagingApi.md#sendemailtosinglerecipient) | **POST** /messaging/v1/email/messages/{messageKey} | sendEmailToSingleRecipient
*TransactionalMessagingApi* | [**sendSmsToMultipleRecipients**](docs/Api/TransactionalMessagingApi.md#sendsmstomultiplerecipients) | **POST** /messaging/v1/sms/messages/ | sendSmsToMultipleRecipients
*TransactionalMessagingApi* | [**sendSmsToSingleRecipient**](docs/Api/TransactionalMessagingApi.md#sendsmstosinglerecipient) | **POST** /messaging/v1/sms/messages/{messageKey} | sendSmsToSingleRecipient


## Documentation For Models

 - [ApiError](docs/Model/ApiError.md)
 - [Asset](docs/Model/Asset.md)
 - [AssetType](docs/Model/AssetType.md)
 - [Attributes](docs/Model/Attributes.md)
 - [Campaign](docs/Model/Campaign.md)
 - [CreateEmailDefinitionContent](docs/Model/CreateEmailDefinitionContent.md)
 - [CreateEmailDefinitionOptionsRequest](docs/Model/CreateEmailDefinitionOptionsRequest.md)
 - [CreateEmailDefinitionRequest](docs/Model/CreateEmailDefinitionRequest.md)
 - [CreateEmailDefinitionSubscriptions](docs/Model/CreateEmailDefinitionSubscriptions.md)
 - [CreateSmsDefinitionContent](docs/Model/CreateSmsDefinitionContent.md)
 - [CreateSmsDefinitionRequest](docs/Model/CreateSmsDefinitionRequest.md)
 - [CreateSmsDefinitionSubscriptions](docs/Model/CreateSmsDefinitionSubscriptions.md)
 - [DeleteQueuedMessagesForSendDefinitionResponse](docs/Model/DeleteQueuedMessagesForSendDefinitionResponse.md)
 - [DeleteSendDefinitionResponse](docs/Model/DeleteSendDefinitionResponse.md)
 - [GetDefinitionSendStatusForRecipientResponse](docs/Model/GetDefinitionSendStatusForRecipientResponse.md)
 - [GetDefinitionSendStatusForRecipientResponseInfo](docs/Model/GetDefinitionSendStatusForRecipientResponseInfo.md)
 - [GetDefinitionsNotSentToRecipientsMessage](docs/Model/GetDefinitionsNotSentToRecipientsMessage.md)
 - [GetDefinitionsNotSentToRecipientsMessageInfo](docs/Model/GetDefinitionsNotSentToRecipientsMessageInfo.md)
 - [GetDefinitionsNotSentToRecipientsResponse](docs/Model/GetDefinitionsNotSentToRecipientsResponse.md)
 - [GetEmailDefinitionsResponse](docs/Model/GetEmailDefinitionsResponse.md)
 - [GetQueueMetricsForSendDefinitionResponse](docs/Model/GetQueueMetricsForSendDefinitionResponse.md)
 - [GetSmsDefinitionsResponse](docs/Model/GetSmsDefinitionsResponse.md)
 - [Recipient](docs/Model/Recipient.md)
 - [SendDefinitionResponseItem](docs/Model/SendDefinitionResponseItem.md)
 - [SendDefinitionToMultipleRecipientsResponse](docs/Model/SendDefinitionToMultipleRecipientsResponse.md)
 - [SendDefinitionToSingleRecipientResponse](docs/Model/SendDefinitionToSingleRecipientResponse.md)
 - [SendEmailToMultipleRecipientsRequest](docs/Model/SendEmailToMultipleRecipientsRequest.md)
 - [SendEmailToSingleRecipientRequest](docs/Model/SendEmailToSingleRecipientRequest.md)
 - [SendSmsContentRequest](docs/Model/SendSmsContentRequest.md)
 - [SendSmsToMultipleRecipientsRequest](docs/Model/SendSmsToMultipleRecipientsRequest.md)
 - [SendSmsToMultipleRecipientsSubscriptionsRequest](docs/Model/SendSmsToMultipleRecipientsSubscriptionsRequest.md)
 - [SendSmsToSingleRecipientRequest](docs/Model/SendSmsToSingleRecipientRequest.md)
 - [SharingProperties](docs/Model/SharingProperties.md)
 - [UpdateEmailDefinitionRequest](docs/Model/UpdateEmailDefinitionRequest.md)
 - [UpdateSmsDefinitionRequest](docs/Model/UpdateSmsDefinitionRequest.md)


## Author

mc_sdk@salesforce.com

