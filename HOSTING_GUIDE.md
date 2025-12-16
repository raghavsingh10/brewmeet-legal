# Legal Documents Hosting Guide

## Quick Setup: GitHub Pages (FREE & Easy)

### Step 1: Create a GitHub Repository
1. Go to [github.com](https://github.com) and create a new repository
2. Name it: `brewmeet-legal` (or any name you prefer)
3. Make it **Public**
4. Check "Add a README file"
5. Click "Create repository"

### Step 2: Upload Your Legal Files
1. Click "Add file" → "Upload files"
2. Drag and drop both:
   - `privacy-policy.html`
   - `terms-of-service.html`
3. Click "Commit changes"

### Step 3: Enable GitHub Pages
1. Go to repository Settings → Pages (left sidebar)
2. Under "Source", select "Deploy from a branch"
3. Select branch: `main` and folder: `/ (root)`
4. Click "Save"
5. Wait 2-3 minutes for deployment

### Step 4: Get Your URLs
Your documents will be available at:
```
https://[your-username].github.io/brewmeet-legal/privacy-policy.html
https://[your-username].github.io/brewmeet-legal/terms-of-service.html
```

Example:
```
https://raghav.github.io/brewmeet-legal/privacy-policy.html
https://raghav.github.io/brewmeet-legal/terms-of-service.html
```

### Step 5: Update Your App
1. Open `src/screens/SettingsScreen.tsx`
2. Find lines with `https://brewmeet.app/privacy` and `https://brewmeet.app/terms`
3. Replace with your GitHub Pages URLs:

```typescript
// Privacy Policy
onPress={() => Linking.openURL('https://[your-username].github.io/brewmeet-legal/privacy-policy.html')}

// Terms of Service
onPress={() => Linking.openURL('https://[your-username].github.io/brewmeet-legal/terms-of-service.html')}
```

---

## Alternative: Use Your Own Domain (brewmeet.app)

If you own `brewmeet.app`, you can host the documents there:

### Option A: Simple Static Hosting
1. Upload files to your web hosting via FTP/cPanel
2. Place them at: `https://brewmeet.app/privacy.html` and `https://brewmeet.app/terms.html`

### Option B: GitHub Pages with Custom Domain
1. Follow Steps 1-3 above
2. In GitHub repo Settings → Pages → Custom domain
3. Enter: `brewmeet.app`
4. Add DNS CNAME record pointing to: `[your-username].github.io`
5. Your URLs will be: `https://brewmeet.app/privacy-policy.html`

---

## Important: Customize Before Publishing!

### Required Changes in Both Documents:

1. **Company Address**
   - Find `[Your Company Address]` in both files
   - Replace with your actual business address
   
2. **Email Addresses** (Optional)
   - Change `privacy@brewmeet.app` to your actual email
   - Change `legal@brewmeet.app` to your actual email
   - Change `support@brewmeet.app` to your actual email
   
3. **Governing Law** (Terms of Service)
   - Find `[Your State/Country]` in Section 15.1
   - Replace with your jurisdiction (e.g., "California, United States")

4. **Review Content**
   - Ensure all information accurately reflects your app
   - Consider having a lawyer review for compliance
   - Update if you add new features or data collection

---

## Testing Your URLs

After hosting, test that your URLs work:

1. Open them in a browser
2. Check on mobile devices
3. Verify they display correctly
4. Test the links in your app (Settings → Privacy Policy / Terms)

---

## App Store Submission

When submitting to Apple:

1. **App Store Connect** → Your App → General Information
2. **Privacy Policy URL**: Enter your privacy policy URL
3. **Terms of Service URL** (optional but recommended)
4. **Support URL**: Enter your support email or website

Apple will check that these URLs:
- ✅ Work and are accessible
- ✅ Are specific to your app (not generic templates)
- ✅ Mention your app name
- ✅ Explain data collection clearly

---

## Updating Legal Documents

When you need to update:

1. **Update the HTML files**
2. **Change the "Last Updated" date**
3. **Re-upload to GitHub (or your hosting)**
4. **Notify users** if changes are significant:
   - In-app notification
   - Email to users
   - Note in next app update

---

## Legal Disclaimer

These templates are provided as a starting point. While they cover common requirements:

- ⚠️ **Not Legal Advice**: These templates do not constitute legal advice
- ⚠️ **Consult a Lawyer**: Consider having an attorney review them
- ⚠️ **Your Responsibility**: You are responsible for compliance with applicable laws
- ⚠️ **Update Regularly**: Laws change; keep your policies current

Recommended: Use services like:
- [TermsFeed](https://www.termsfeed.com/)
- [Termly](https://termly.io/)
- [IUB Beni](https://www.iubenda.com/)

These services can generate customized, legally reviewed documents for $20-50/year.

---

## Checklist

- [ ] Customize company address in both documents
- [ ] Update email addresses (if needed)
- [ ] Set governing law/jurisdiction
- [ ] Upload to GitHub or your hosting
- [ ] Enable GitHub Pages
- [ ] Test URLs in browser and on mobile
- [ ] Update SettingsScreen.tsx with correct URLs
- [ ] Test links in the app
- [ ] Add URLs to App Store Connect
- [ ] (Optional) Have a lawyer review

---

## Support

Need help?
- GitHub Pages Docs: https://docs.github.com/pages
- Questions: Open an issue in your repo
- Legal Questions: Consult an attorney

---

**Quick Action**: If you just want to test, use GitHub Pages now. You can always move to a custom domain later!
