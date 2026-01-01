# Custom Domain DNS Setup for autosave.pithyprint.com

## GitHub Pages Configuration

✅ **CNAME file created**: The repository now includes a `CNAME` file with `autosave.pithyprint.com`

## DNS Configuration Required

You need to add DNS records with your domain provider (wherever `pithyprint.com` is registered).

### Option 1: CNAME Record (Recommended)

Add a **CNAME record** in your DNS settings:

- **Type**: `CNAME`
- **Name/Host**: `autosave`
- **Value/Target**: `mattSherwood.github.io`
- **TTL**: 3600 (or default)

**Note**: For root domains, use A records. For subdomains like `autosave.pithyprint.com`, use CNAME.

### Option 2: A Records (Alternative)

If CNAME doesn't work or you prefer A records, use these GitHub Pages IP addresses:

- **Type**: `A`
- **Name/Host**: `autosave`
- **Value/Target**: One of these IPs:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- **TTL**: 3600 (or default)

Add all 4 A records (one for each IP) for redundancy.

## Enable Custom Domain in GitHub

1. Go to: https://github.com/MattSherwood/AutoSave-Web/settings/pages
2. In the "Custom domain" section, enter: `autosave.pithyprint.com`
3. Check "Enforce HTTPS" (recommended)
4. Save

GitHub will automatically verify the domain once DNS propagates.

## DNS Propagation

- DNS changes typically take **5-60 minutes** to propagate
- Can take up to **24-48 hours** in some cases
- You can check propagation with: https://dnschecker.org/

## Verification

After DNS propagates and GitHub verifies:

1. Visit: `https://autosave.pithyprint.com`
2. Your site should load
3. GitHub will show "Verified" in the Pages settings

## Troubleshooting

If the domain doesn't work after 24 hours:

1. Verify DNS records are correct
2. Check that CNAME file exists in the repo (it does)
3. Ensure GitHub Pages is enabled for the repository
4. Verify domain in GitHub Pages settings
5. Check DNS propagation: https://dnschecker.org/#CNAME/autosave.pithyprint.com

## Notes

- The `CNAME` file in the repo root tells GitHub which custom domain to use
- GitHub will automatically provision SSL certificates for your custom domain
- HTTPS will be enforced once verified

