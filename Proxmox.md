# Proxmox (PVE) with Domeneshop's DNS API

Thanks to an enterprising customer, we have information on how to configure Proxmox's ACME DNS API plugin for use with Domeneshop's API.

The Proxmox configuration is **case sensitive**.

## Prerequisite
Please note that you need to manually add a DNS A record with your local IP address (likely RFC 1918, e.g. `10.0.1.42`) for the domain you will be controlling DNS for.

## API Data
In the Datacenter node's ACME GUI, add the following, substituting your actual API token and secret for `[API token]` and `[API secret]`:

<code>
DOMENESHOP_Token=[API token]
DOMENESHOP_Secret=[API secret]
</code>

### Example

<code>
DOMENESHOP_Token=snjsbX1NjXkDpy5C
DOMENESHOP_Secret=snjsbX1NjXkDpy5CsnjsbX1NjXkDpy5CsnjsbX1NjXkDpy5CsnjsbX1NjXkDpy5C
</code>

### Note: do not trust AI suggestions!
Google Gemini and ChatGPT have been caught suggesting the following, all of which will fail:
 - quoted values for token and secret - **wrong, use no quotes**
 - only UPPERCASE letters in key labels - **wrong, type them exactly as above**
 - only lowercase letters in key labels - **wrong, type them exactly as above**
 - using colon (`:`) instead of equals (`=`) - **wrong, use the equals sign, no spaces, exactly as above**
