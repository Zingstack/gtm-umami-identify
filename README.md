# Umami Analytics - Identify

A Google Tag Manager tag template for identifying users in [Umami Analytics](https://umami.is).

> Built by [Zingstack](https://zingstack.com) · Not an official Umami product

---

## Requirements

- Umami Analytics installed on your website (v2.13.0 or later)
- The Umami tracker script must be loaded **before** this tag fires

## Installation

1. Download `template.tpl`
2. In GTM go to **Templates** → **Tag Templates** → **New**
3. Click `···` → **Import**
4. Select the `template.tpl` file
5. Save the template

## Usage

Create a new tag using the **Umami Analytics - Identify** template:

| Field | Required | Description |
|-------|----------|-------------|
| Distinct ID | — | A unique identifier for the user (e.g. user ID, email) |
| Session data | — | Optional key/value pairs saved to the session |

At least one of the two fields must be filled in.

### Example

| Key | Value |
|-----|-------|
| `name` | `Max Mustermann` |
| `email` | `max@example.com` |
| `plan` | `core` |

## When to use

Call this tag after a user has identified themselves – typically after a form submit or login event. Use a Custom Event trigger in GTM that fires when you push an identify event to the dataLayer.

## Known limitations

The `identify` feature requires Umami v2.13.0 or later. Session stitching (merging anonymous and identified sessions) is currently being worked on by the Umami team.

## Related Templates

- [Umami Analytics - Track Event](https://github.com/Zingstack/gtm-umami-track-event)

## License

Apache 2.0
