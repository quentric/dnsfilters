# DNS Filters

Filter Lists for DNS queries compatible with AdGuard Home and Pi-hole.

## Available Lists

### Blocklist (`blocklist.txt`)
A curated list of domains to block, including:
- Advertising networks
- Tracking and analytics services
- Known malware and phishing domains
- Intrusive social media trackers

### Allowlist (`allowlist.txt`)
A list of domains that should be allowed, including:
- Essential services (Windows Update, Apple Services)
- Popular legitimate websites
- CDN and infrastructure services
- Streaming and email providers

## Usage

### With Pi-hole

1. **Blocklist**: 
   - Navigate to Pi-hole Admin > Group Management > Adlists
   - Add the raw URL to `blocklist.txt`
   - Update gravity

2. **Allowlist**:
   - Navigate to Pi-hole Admin > Whitelist
   - Add domains from `allowlist.txt` manually or import

### With AdGuard Home

1. **Blocklist**:
   - Navigate to Filters > DNS blocklists
   - Add the raw URL to `blocklist.txt`
   - Click "Add blocklist"

2. **Allowlist**:
   - Navigate to Filters > DNS allowlists
   - Add the raw URL to `allowlist.txt`
   - Click "Add allowlist"

## Format

Both lists use the standard hosts file format compatible with both Pi-hole and AdGuard Home:
- One domain per line
- Comments start with `#`
- Blocklist uses `0.0.0.0 domain.com` format
- Allowlist uses plain domain format

## Contributing

Feel free to suggest additions or removals by opening an issue or pull request.

## License

See [LICENSE](LICENSE) file for details.
