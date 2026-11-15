# Lab 3 — Component Modelling & Architectural Pattern Selection

**Scenario:** Self-Service Coffee Kiosk
**Selected architecture:** Layered Architecture

## Deliverables

- `diagram/coffee_kiosk_component_diagram.png` — diagram image for submission.
- `diagram/coffee_kiosk_component_diagram.pdf` — printable diagram.
- `diagram/coffee_kiosk_component_diagram.svg` — editable vector source.
- `docs/Architecture_Justification.docx` — one-page editable justification.
- `docs/Architecture_Justification.pdf` — one-page PDF for submission.

## Components

1. Touchscreen UI
2. Order Manager (given)
3. Payment Service (given)
4. Menu & Pricing Repository
5. Receipt Service
6. Receipt Printer Adapter
7. External Card Payment Gateway

## Architectural decision

Layered architecture is appropriate for a single kiosk because it separates UI, business workflow, and data/device access without the operational overhead of microservices. The diagram shows provided interfaces (lollipop), required interfaces (socket), and labelled service connectors.

## Important security note

The gateway integration is conceptual: a real implementation must use a compliant payment provider, TLS, tokenization/hosted payment capture, and must not store CVV or raw card data.
