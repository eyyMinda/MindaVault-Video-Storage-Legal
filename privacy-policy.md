# Privacy policy — MindaVault

**Last updated:** May 27, 2026

This privacy policy describes how **MindaVault** (“the App”, “we”, “us”) handles information when merchants install and use our Shopify embedded application.

The App is operated by the developer reachable at **contact@eyyminda.com** (“Developer”).

---

## Summary

- We process **store and app data** needed to provide video hosting and storage for your Shopify shop.
- We do **not** collect or store your customers’ personal information (names, emails, addresses, order history, etc.).
- Video files you upload are stored on **Cloudflare R2** and are served via **public URLs** you choose to embed on your storefront or elsewhere.
- When you uninstall the App or Shopify sends a **shop/redact** request, we delete your shop’s data and stored files.

---

## Who this policy applies to

This policy applies to **merchants** (Shopify store owners and staff) who install the App. It does not apply to your store’s end customers (buyers), because the App does not collect their personal data.

If you embed App-hosted videos on your storefront, you are responsible for your own privacy notices to buyers regarding those embeds and any analytics or players you add outside the App.

---

## Information we collect

### From Shopify (when you install or use the App)

- Shop domain and shop identifier  
- App installation and session data required for authentication  
- Subscription and billing status related to App plans (via Shopify Billing)

We request **minimal API scopes** (typically none beyond what is required for an embedded app to authenticate). The App does not read your products, orders, or customers through the Shopify Admin API for its core features.

### Data you provide in the App

- Video files and optional thumbnails you upload  
- Display names and metadata we store for those files (file name, size, duration, public URL, upload date)  
- Support messages you send us by email

### Automatically collected

- Technical logs from our hosting provider (e.g. request timestamps, errors) — not used to profile merchants  
- Storage usage and quota calculations for your shop

### What we do not collect

- End-customer personal data (PII)  
- Payment card details (handled by Shopify)  
- Browsing behavior of your store visitors through the App

---

## How we use information

We use the information above to:

- Provide upload, storage, quota, and public link features  
- Process subscriptions and enforce plan limits  
- Operate security and abuse prevention (e.g. file type checks, rate limits)  
- Respond to support requests  
- Comply with legal obligations and Shopify’s platform requirements  

We do not sell merchant data. We do not use merchant data for advertising.

---

## Where data is stored and processed

| Provider | Role | Location |
| -------- | ---- | -------- |
| **Shopify** | Platform, auth, billing | As per Shopify |
| **Vercel** | Application hosting | United States / global edge |
| **Supabase** | PostgreSQL database (metadata) | Region of your Supabase project |
| **Cloudflare R2** | Video and thumbnail file storage | Cloudflare network |

Data is isolated **per shop** in our database and object storage (separate key prefixes per store).

---

## Public video URLs

Videos you upload receive a **stable public URL** intended for embedding in themes, page builders, or landing pages. Anyone with that URL may be able to view the file unless you protect it elsewhere (e.g. unlisted pages, access control on your site). Do not upload confidential content unless you accept this behavior.

---

## Retention and deletion

- **Active installation:** We retain your videos and metadata while the App is installed and you have not deleted files.  
- **You delete a video:** The file is removed from storage and the link stops working.  
- **You uninstall the App:** We delete your shop’s videos, metadata, and related records (via the `app/uninstalled` webhook).  
- **Shop data erasure:** When Shopify sends a **shop/redact** compliance webhook, we delete the same shop data.  
- **Customer requests:** We do not hold customer PII; `customers/data_request` and `customers/redact` webhooks are acknowledged with no customer data to export or erase.

Backups, if any, are overwritten in the normal course of operation; we do not maintain long-term archives of deleted shop content.

---

## Legal bases (EEA/UK merchants)

Where applicable, we rely on:

- **Contract** — to provide the App you installed  
- **Legitimate interests** — security, abuse prevention, and improving reliability  
- **Legal obligation** — where required by law or Shopify  

---

## Your rights

Depending on your location, you may have rights to access, correct, delete, or restrict processing of your personal data. Because we primarily process **shop/business** data tied to your store, contact us at **contact@eyyminda.com** from your store’s admin email and include your shop domain.

We will respond within a reasonable time and in line with applicable law.

---

## Security

We use industry-standard practices including HTTPS, authenticated admin access, presigned uploads with limited expiry, shop-scoped storage paths, and webhook signature verification. No method of transmission or storage is 100% secure; use strong passwords on your Shopify account and notify us if you suspect unauthorized access.

---

## Children

The App is for businesses using Shopify. It is not directed at children under 16.

---

## Changes to this policy

We may update this policy from time to time. We will post the new version on this page and update the “Last updated” date. Continued use of the App after changes constitutes acceptance of the revised policy where permitted by law.

---

## Contact

**Email:** [contact@eyyminda.com](mailto:contact@eyyminda.com)

**Published at:** [https://eyyminda.github.io/Extended-Video-Storage-Legal/privacy-policy](https://eyyminda.github.io/Extended-Video-Storage-Legal/privacy-policy) (source copy in this repo’s `docs/` folder; sync to [Extended-Video-Storage-Legal](https://github.com/eyyMinda/Extended-Video-Storage-Legal) when you change this file).
