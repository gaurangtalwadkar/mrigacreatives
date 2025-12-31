---
description: Custom Domain Setup for GitHub Pages
---

# How to Setup mrigacreatives.com with GitHub Pages

This guide outlines the steps to purchase a custom domain (`mrigacreatives.com`) and link it to your existing GitHub Pages site.

## 1. Purchase the Domain (~$10-15/year)

You need to buy the domain name from a registrar. Popular options include:

*   **Namecheap** (Recommended for developers)
*   **Google Domains** (Integration with Google services)
*   **GoDaddy** (Popular, easy UI)

**Steps:**
1.  Go to the registrar's website.
2.  Search for `mrigacreatives.com`.
3.  Add it to your cart and complete the purchase.
4.  *Note: Prices usually range from $10 to $15 USD per year.*

## 2. Configure DNS Settings

Once you own the domain, you need to point it to GitHub's servers.

1.  Log in to your registrar's dashboard.
2.  Find the **DNS Settings** or **DNS Management** page for your domain.
3.  Add the following **A Records** (to point the root domain):
    *   **Type:** `A` | **Host/Name:** `@` | **Value:** `185.199.108.153`
    *   **Type:** `A` | **Host/Name:** `@` | **Value:** `185.199.109.153`
    *   **Type:** `A` | **Host/Name:** `@` | **Value:** `185.199.110.153`
    *   **Type:** `A` | **Host/Name:** `@` | **Value:** `185.199.111.153`

4.  Add a **CNAME Record** (to point `www` subdomain):
    *   **Type:** `CNAME` | **Host/Name:** `www` | **Value:** `gaurangtalwadkar.github.io`

## 3. Configure GitHub Pages

Tell GitHub that you want to use this custom domain.

1.  Go to your repository settings on GitHub (`gaurangtalwadkar/mrigacreatives`).
2.  Navigate to **Pages** in the sidebar.
3.  Under **Custom domain**, type `mrigacreatives.com`.
4.  Click **Save**.
5.  GitHub will check the DNS settings. Once verified (might take up to 24 hours to propagate), check the **"Enforce HTTPS"** box.
6.  *Important:* This will create a `CNAME` file in your repository. Do not delete it.

## 4. Updates for AdMob

Since your domain changes from `gaurangtalwadkar.github.io` to `mrigacreatives.com`:

1.  **AdMob Console:** Update your app settings in AdMob to point to `mrigacreatives.com`.
2.  **app-ads.txt:**
    *   Ensure your `app-ads.txt` is accessible at `https://mrigacreatives.com/app-ads.txt`.
    *   Since you set the custom domain on your GitHub Pages repo, this should happen automatically!
