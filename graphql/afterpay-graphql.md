# Afterpay GraphQL Schema

This is a conceptual GraphQL schema for the Afterpay (Clearpay) Buy Now Pay Later (BNPL) API. Afterpay is a payment platform that allows merchants to offer installment-based payment options to consumers. The schema models the core domain objects and operations available through the Afterpay merchant API.

## Overview

Afterpay provides merchants with APIs to integrate BNPL payment flows including:

- **Checkout**: Create and manage Afterpay checkout sessions
- **Payments**: Authorize, capture, void, and refund payments
- **Orders**: Manage order details and status
- **Consumers**: Verify consumer eligibility and decisions
- **Configuration**: Retrieve merchant configuration and supported plans
- **Settlements**: Access settlement and reconciliation data
- **Webhooks**: Subscribe to payment lifecycle events

## Source

- Human URL: https://developers.afterpay.com/afterpay-online/reference
- Base URL: https://api.afterpay.com

## Schema File

See [afterpay-schema.graphql](afterpay-schema.graphql) for the full type definitions.

## Key Types

| Type | Description |
|------|-------------|
| Order | Top-level order object tying checkout to payment |
| OrderDetails | Full order metadata including items and consumer |
| OrderStatus | Enum of order lifecycle states |
| OrderAmount | Monetary amount with currency |
| OrderToken | Unique token identifying an Afterpay order |
| Checkout | Checkout session created by merchant |
| CheckoutDetails | Full details of a checkout session |
| CheckoutStatus | Enum of checkout states |
| CheckoutURL | Redirect URL for consumer approval flow |
| Capture | Payment capture after consumer approval |
| CaptureDetails | Details of a capture event |
| Void | Cancellation of an authorized payment |
| VoidDetails | Details of a void operation |
| Refund | Refund issued against a captured payment |
| RefundDetails | Full refund metadata |
| RefundAmount | Amount and currency for a refund |
| Payment | Core payment record |
| PaymentDetails | Expanded payment record with events |
| PaymentStatus | Enum of payment lifecycle states |
| PaymentEvent | Individual event in payment history |
| Consumer | Afterpay consumer account |
| ConsumerDetails | Full consumer profile |
| ConsumerVerification | Consumer identity verification status |
| Decision | Afterpay credit decision for a consumer |
| DecisionDetails | Full decision record including reason codes |
| DecisionStatus | Enum of decision outcomes |
| Item | Line item in an order |
| ItemDetails | Full item metadata |
| ItemCategory | Product category classification |
| ItemQuantity | Quantity and unit for an item |
| Discount | Discount applied to an order |
| DiscountDetails | Full discount metadata |
| Shipping | Shipping record for an order |
| ShippingDetails | Full shipping metadata |
| Address | Physical address |
| ShippingCarrier | Carrier used for shipment |
| ShippingTracking | Tracking number and URL |
| Merchant | Merchant account record |
| MerchantDetails | Full merchant profile |
| MerchantPlan | BNPL plan offered to merchant |
| Configuration | Merchant-level Afterpay configuration |
| Installment | Single installment in a payment schedule |
| InstallmentSchedule | Full schedule of installments |
| PaymentInstallment | Consumer-facing installment with status |
| Settlement | Settlement batch record |
| SettlementDetails | Full settlement with line items |
| Webhook | Registered webhook endpoint |
| WebhookEvent | Webhook event payload |
| APIKey | Merchant API key record |
| Token | Authentication or session token |
