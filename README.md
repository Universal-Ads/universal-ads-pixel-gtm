# Universal Ads Pixel — GTM Community Template

Official Google Tag Manager Community Template for the Universal Ads Pixel. Enables no-code UA Pixel deployment and event tracking directly from Google Tag Manager.

---

## Overview

This template loads the Universal Ads Pixel SDK and fires conversion events without requiring any custom JavaScript. It is designed for advertisers and agencies managing UA Pixel implementation through Google Tag Manager.

## Prerequisites

Before configuring this template, you must:

1. Create a UA Pixel in Universal Ads Ads Manager
2. Select the events you want to track within Ads Manager
3. Copy your **Pixel ID** and **Access Token** from the pixel detail view in Ads Manager

> Events configured in GTM but not enabled in Ads Manager will not be reported or attributed in the platform.

## Installation

1. In Google Tag Manager, navigate to **Templates → Tag Templates**
2. Click **Search Gallery** and search for **Universal Ads Pixel**
3. Select the template and click **Add to workspace**

## Configuration

| Field | Required | Description |
|---|---|---|
| Pixel ID | Yes | 36-character identifier generated when your UA Pixel is created |
| Access Token | Yes | Unique token generated when your UA Pixel is created |
| Event Type | Yes | The conversion event to fire |
| Event Parameters | No | Additional data to include with the event |
| Send Page View on Init | No | Also fires a `page_view` event when this tag fires |

## Supported Events

| Event | Value |
|---|---|
| Page View | `page_view` |
| Content View | `content_view` |
| Product View | `product_view` |
| Search | `search` |
| Schedule Appointment | `schedule_appointment` |
| Sign In | `sign_in` |
| Sign Up | `sign_up` |
| Start Trial | `start_trial` |
| View Cart | `view_cart` |
| Wish List | `wish_list` |
| Purchase | `purchase` |
| Start Checkout | `checkout_start` |
| Add to Cart | `add_to_cart` |
| Add Payment Info | `add_payment_info` |
| Add Address Info | `add_address_info` |
| Subscribe | `subscribe` |
| Custom Event 1 | `custom_event_1` |
| Custom Event 2 | `custom_event_2` |

## Supported Parameters

| Parameter | Key |
|---|---|
| Price | `price` |
| Currency | `currency` |
| Order ID | `order_id` |
| Description | `description` |
| User ID | `user_id` |
| User Email | `user_name` |
| Content ID | `content_id` |
| Item Quantity | `item_quantity` |

## Usage Notes

- The UA SDK loads once per page regardless of how many UA Pixel tags fire
- `startWithConfig` executes only once per page — subsequent tags skip initialization automatically
- Empty or undefined parameter values are ignored and not included in the event payload
- The **Send Page View on Init** checkbox is disabled by default to prevent unintentional duplicate page view events

## Support

To report a bug or request a feature, open an issue in this repository.

## License

Apache License 2.0. See [LICENSE](LICENSE) for details.
