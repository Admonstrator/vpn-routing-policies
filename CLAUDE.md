# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository manages VPN routing policies for GL.iNET routers, specifically for excluding certain domains from VPN tunnels. Main usage is in Germany via Mullvad VPN to access streaming services that are geo-blocked when using VPN.

## File Structure

- `policies.txt` - Core domain policies organized by service categories (PERSONAL, DISNEYPLUS, RTL+)
- `policies_complete.txt` - Auto-generated combined file (local + external policies)
- `.github/workflows/update-policies.yml` - Daily automation workflow

## Domain Policy Format

Policies use a simple domain-per-line format with comment sections:
```
#START SERVICENAME#
domain.com
subdomain.domain.com
#END SERVICENAME#
```

## Automation

The repository includes a GitHub Actions workflow that:
- Runs daily at midnight UTC
- Downloads external policies from `https://lou.h4ck.me/vpn_bypass.txt`
- Combines them with local `policies.txt` 
- Generates `policies_complete.txt`
- Auto-commits changes if content differs

Manual workflow triggers are supported via GitHub Actions UI.

## Usage Context

When users reference GL.iNET router configuration, policies are copied into the "Custom Domain" field of the VPN policy settings. Personal policies are marked as such and may not be relevant for all users.