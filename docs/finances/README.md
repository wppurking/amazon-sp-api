# swagger-java-client

Selling Partner API for Finances
- API version: v0
  - Build date: 2020-12-15T20:01:58.583+08:00

The Selling Partner API for Finances helps you obtain financial information relevant to a seller's business. You can obtain financial events for a given order, financial event group, or date range without having to wait until a statement period closes. You can also obtain financial event groups for a given date range.

  For more information, please visit [https://sellercentral.amazon.com/gp/mws/contactus.html](https://sellercentral.amazon.com/gp/mws/contactus.html)

*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>io.swagger</groupId>
  <artifactId>swagger-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/swagger-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.amazon.spapi.finances.*;
import com.amazon.spapi.finances.auth.*;
import com.amazon.spapi.model.finances.*;
import com.amazon.spapi.finances.api.DefaultApi;

import java.io.File;
import java.util.*;

public class DefaultApiExample {

    public static void main(String[] args) {
        
        DefaultApi apiInstance = new DefaultApi();
        Integer maxResultsPerPage = 100; // Integer | The maximum number of results to return per page.
        OffsetDateTime financialEventGroupStartedBefore = OffsetDateTime.now(); // OffsetDateTime | A date used for selecting financial event groups that opened before (but not at) a specified date and time, in ISO 8601 format. The date-time  must be later than FinancialEventGroupStartedAfter and no later than two minutes before the request was submitted. If FinancialEventGroupStartedAfter and FinancialEventGroupStartedBefore are more than 180 days apart, no financial event groups are returned.
        OffsetDateTime financialEventGroupStartedAfter = OffsetDateTime.now(); // OffsetDateTime | A date used for selecting financial event groups that opened after (or at) a specified date and time, in ISO 8601 format. The date-time must be no later than two minutes before the request was submitted.
        String nextToken = "nextToken_example"; // String | A string token returned in the response of your previous request.
        try {
            ListFinancialEventGroupsResponse result = apiInstance.listFinancialEventGroups(maxResultsPerPage, financialEventGroupStartedBefore, financialEventGroupStartedAfter, nextToken);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#listFinancialEventGroups");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://sellingpartnerapi-na.amazon.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**listFinancialEventGroups**](DefaultApi.md#listFinancialEventGroups) | **GET** /finances/v0/financialEventGroups | 
*DefaultApi* | [**listFinancialEvents**](DefaultApi.md#listFinancialEvents) | **GET** /finances/v0/financialEvents | 
*DefaultApi* | [**listFinancialEventsByGroupId**](DefaultApi.md#listFinancialEventsByGroupId) | **GET** /finances/v0/financialEventGroups/{eventGroupId}/financialEvents | 
*DefaultApi* | [**listFinancialEventsByOrderId**](DefaultApi.md#listFinancialEventsByOrderId) | **GET** /finances/v0/orders/{orderId}/financialEvents | 


## Documentation for Models

 - [AdjustmentEvent](AdjustmentEvent.md)
 - [AdjustmentEventList](AdjustmentEventList.md)
 - [AdjustmentItem](AdjustmentItem.md)
 - [AdjustmentItemList](AdjustmentItemList.md)
 - [AffordabilityExpenseEvent](AffordabilityExpenseEvent.md)
 - [AffordabilityExpenseEventList](AffordabilityExpenseEventList.md)
 - [ChargeComponent](ChargeComponent.md)
 - [ChargeComponentList](ChargeComponentList.md)
 - [ChargeInstrument](ChargeInstrument.md)
 - [ChargeInstrumentList](ChargeInstrumentList.md)
 - [CouponPaymentEvent](CouponPaymentEvent.md)
 - [CouponPaymentEventList](CouponPaymentEventList.md)
 - [Currency](Currency.md)
 - [DebtRecoveryEvent](DebtRecoveryEvent.md)
 - [DebtRecoveryEventList](DebtRecoveryEventList.md)
 - [DebtRecoveryItem](DebtRecoveryItem.md)
 - [DebtRecoveryItemList](DebtRecoveryItemList.md)
 - [DirectPayment](DirectPayment.md)
 - [DirectPaymentList](DirectPaymentList.md)
 - [Error](../Error.md)
 - [ErrorList](../ErrorList.md)
 - [FBALiquidationEvent](FBALiquidationEvent.md)
 - [FBALiquidationEventList](FBALiquidationEventList.md)
 - [FeeComponent](FeeComponent.md)
 - [FeeComponentList](FeeComponentList.md)
 - [FinancialEventGroup](FinancialEventGroup.md)
 - [FinancialEventGroupList](FinancialEventGroupList.md)
 - [FinancialEvents](FinancialEvents.md)
 - [ImagingServicesFeeEvent](ImagingServicesFeeEvent.md)
 - [ImagingServicesFeeEventList](ImagingServicesFeeEventList.md)
 - [ListFinancialEventGroupsPayload](ListFinancialEventGroupsPayload.md)
 - [ListFinancialEventGroupsResponse](ListFinancialEventGroupsResponse.md)
 - [ListFinancialEventsPayload](ListFinancialEventsPayload.md)
 - [ListFinancialEventsResponse](ListFinancialEventsResponse.md)
 - [LoanServicingEvent](LoanServicingEvent.md)
 - [LoanServicingEventList](LoanServicingEventList.md)
 - [NetworkComminglingTransactionEvent](NetworkComminglingTransactionEvent.md)
 - [NetworkComminglingTransactionEventList](NetworkComminglingTransactionEventList.md)
 - [PayWithAmazonEvent](PayWithAmazonEvent.md)
 - [PayWithAmazonEventList](PayWithAmazonEventList.md)
 - [ProductAdsPaymentEvent](ProductAdsPaymentEvent.md)
 - [ProductAdsPaymentEventList](ProductAdsPaymentEventList.md)
 - [Promotion](Promotion.md)
 - [PromotionList](PromotionList.md)
 - [RemovalShipmentEvent](RemovalShipmentEvent.md)
 - [RemovalShipmentEventList](RemovalShipmentEventList.md)
 - [RemovalShipmentItem](RemovalShipmentItem.md)
 - [RemovalShipmentItemList](RemovalShipmentItemList.md)
 - [RentalTransactionEvent](RentalTransactionEvent.md)
 - [RentalTransactionEventList](RentalTransactionEventList.md)
 - [RetrochargeEvent](RetrochargeEvent.md)
 - [RetrochargeEventList](RetrochargeEventList.md)
 - [SAFETReimbursementEvent](SAFETReimbursementEvent.md)
 - [SAFETReimbursementEventList](SAFETReimbursementEventList.md)
 - [SAFETReimbursementItem](SAFETReimbursementItem.md)
 - [SAFETReimbursementItemList](SAFETReimbursementItemList.md)
 - [SellerDealPaymentEvent](SellerDealPaymentEvent.md)
 - [SellerDealPaymentEventList](SellerDealPaymentEventList.md)
 - [SellerReviewEnrollmentPaymentEvent](SellerReviewEnrollmentPaymentEvent.md)
 - [SellerReviewEnrollmentPaymentEventList](SellerReviewEnrollmentPaymentEventList.md)
 - [ServiceFeeEvent](ServiceFeeEvent.md)
 - [ServiceFeeEventList](ServiceFeeEventList.md)
 - [ShipmentEvent](ShipmentEvent.md)
 - [ShipmentEventList](ShipmentEventList.md)
 - [ShipmentItem](ShipmentItem.md)
 - [ShipmentItemList](ShipmentItemList.md)
 - [SolutionProviderCreditEvent](SolutionProviderCreditEvent.md)
 - [SolutionProviderCreditEventList](SolutionProviderCreditEventList.md)
 - [TDSReimbursementEvent](TDSReimbursementEvent.md)
 - [TDSReimbursementEventList](TDSReimbursementEventList.md)
 - [TaxWithheldComponent](TaxWithheldComponent.md)
 - [TaxWithheldComponentList](TaxWithheldComponentList.md)
 - [TrialShipmentEvent](TrialShipmentEvent.md)
 - [TrialShipmentEventList](TrialShipmentEventList.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



