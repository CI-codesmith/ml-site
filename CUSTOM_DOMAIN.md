# Custom Domain Setup Guide

**Two Options:** Use a custom domain for GitHub Pages + Gamma, or keep free URLs.

---

## Option 1: Custom Domain for GitHub Pages

### Prerequisites
- Own/purchase a domain (e.g., `machinelearningcourse.com`)
- Access to domain registrar (GoDaddy, Namecheap, etc.)

### Step 1: Configure GitHub Pages

1. Go to: https://github.com/CI-codesmith/ml-site/settings/pages
2. Under "Custom domain," enter your domain
3. Example: `machinelearningcourse.com`
4. Click Save

### Step 2: Update DNS Records

Contact your domain registrar and add:

**Option A: Using A Records (Most Common)**
```
A record pointing to:
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**Option B: Using CNAME Record**
```
CNAME record:
CI-codesmith.github.io
```

### Step 3: Enable HTTPS

GitHub automatically enables HTTPS once DNS is configured.
- Go back to Pages settings
- Check "Enforce HTTPS"

### Step 4: Wait for DNS Propagation
- DNS changes take 24-48 hours to fully propagate
- Your site will be live at: `https://machinelearningcourse.com`

---

## Option 2: Custom Domain for Gamma Site

### Step 1: Access Gamma Settings

1. Go to your Gamma site
2. Click **Settings** (gear icon)
3. Select **Custom domain**

### Step 2: Enter Your Domain

1. In Gamma settings, click **Add custom domain**
2. Enter your domain (e.g., `gamma.machinelearningcourse.com`)
3. Click Verify

### Step 3: Update DNS at Registrar

Gamma will provide DNS records. Add them:
```
CNAME record:
your-domain.gamma.app
```

Or check Gamma dashboard for exact records to add.

### Step 4: Verify Domain

Return to Gamma settings and click "Verify domain"
Once verified, your Gamma site is live on the custom domain.

---

## Recommended Setup

### Best Practice: Use Subdomains

**Main Site (GitHub Pages - Educational Content):**
```
machinelearningcourse.com → GitHub Pages (ml-site)
```

**Interactive Overview (Gamma):**
```
overview.machinelearningcourse.com → Gamma site
```

This keeps content organized:
- Main domain = Theory & practicals
- Subdomain = Interactive overview

---

## DNS Record Examples

### GoDaddy

1. Login to GoDaddy
2. Go to **DNS Management**
3. Add A Records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   (repeat for all 4 IPs)
   ```

### Namecheap

1. Login to Namecheap
2. Go to **Advanced DNS**
3. Add A Records (same as above)

### Other Registrars

Instructions are similar - look for "DNS Management" or "DNS Settings"

---

## Verify It Works

After 24-48 hours:

1. Visit your domain: `https://machinelearningcourse.com`
2. Should load your ML course site
3. Check HTTPS works (green lock icon)

If not working:
- Wait longer (up to 48 hours)
- Verify DNS records are correct
- Check GitHub Pages settings again

---

## Free Alternative

**Keep free URLs instead:**
- GitHub Pages: `CI-codesmith.github.io/ml-site`
- Gamma Site: `msbte-ml-61uo5hn.gamma.site`

No DNS configuration needed, no domain purchase required.

---

## FAQ

**Q: Which domain registrar should I use?**
A: GoDaddy, Namecheap, or Google Domains all work. Use whichever you prefer.

**Q: How much does a domain cost?**
A: Typically $10-15/year for .com domains.

**Q: Can I change the domain later?**
A: Yes, anytime in GitHub Pages and Gamma settings.

**Q: How long until the domain works?**
A: 2-48 hours for DNS propagation. Usually 2-6 hours.

**Q: Do I need HTTPS?**
A: GitHub Pages provides free HTTPS automatically.

---

## Troubleshooting

### Domain not working after 48 hours

1. Check DNS records:
   ```bash
   nslookup machinelearningcourse.com
   ```

2. Verify GitHub Pages settings
3. Re-add the domain in GitHub Pages settings
4. Contact registrar support

### HTTPS not enabling

1. Wait 5-10 minutes after adding domain
2. Remove and re-add domain in GitHub Pages
3. Check "Enforce HTTPS" checkbox

---

[← Back to Deployment](DEPLOYMENT.md)
