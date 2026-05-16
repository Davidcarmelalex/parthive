# PartHive 🔧

> A premium automotive sourcing ecosystem that bridges UAE vehicle owners and certified workshops with AI-driven part diagnostics and seamless doorstep fulfillment.

## Overview

PartHive connects UAE vehicle owners with certified workshops, leveraging AI to diagnose vehicle issues, identify required parts, and fulfill orders with doorstep delivery.

## Data Models

### Vehicle
Tracks user-owned vehicles in the UAE.
| Field | Type | Description |
|-------|------|-------------|
| make | string | Vehicle manufacturer |
| model | string | Vehicle model |
| year | string | Manufacturing year |
| vin | string | Vehicle Identification Number |
| plate_number | string | UAE plate number |
| emirate | string | Emirates (Dubai, Abu Dhabi, etc.) |
| image_url | string | Vehicle photo |

### Workshop
Certified partner workshops across the UAE.
| Field | Type | Description |
|-------|------|-------------|
| name | string | Workshop name |
| location | string | Address |
| emirate | string | Emirates |
| specialization | string | Area of expertise |
| rating | number | Average rating |
| reviews_count | number | Number of reviews |
| is_certified | boolean | Certification status |
| phone | string | Contact number |
| image_url | string | Workshop photo |
| discount_tier | string | Partner discount level |

### WorkshopReport
AI-generated diagnostic reports from workshops.
| Field | Type | Description |
|-------|------|-------------|
| vehicle_id | string | Associated vehicle |
| file_url | string | Report document URL |
| status | string | Report status |
| diagnosis | string | AI diagnosis summary |
| parts_needed | array | List of required parts |
| total_market_price | number | Market price estimate |
| total_our_price | number | PartHive discounted price |
| delivery_preference | string | Delivery method |
| notes | string | Additional notes |

### Order
Fulfillment orders for parts.
| Field | Type | Description |
|-------|------|-------------|
| report_id | string | Associated report |
| vehicle_id | string | Associated vehicle |
| status | string | Order status |
| delivery_type | string | Delivery or pickup |
| delivery_address | string | Delivery location |
| workshop_id | string | Fulfilling workshop |
| total_amount | number | Order total |
| savings | number | Amount saved vs market |
| tracking_number | string | Shipment tracking |
| estimated_delivery | string | ETA |
| items | array | Parts ordered |

## Built With
- Base44 (no-code app platform)
- AI diagnostics integration
- UAE automotive ecosystem

