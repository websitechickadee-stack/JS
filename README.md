# Vue Basic

[Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview) allows you to easily build [Vue.js](https://vuejs.org/) apps in minutes. Use this repo with the [Vue quickstart](https://docs.microsoft.com/azure/static-web-apps/getting-started?tabs=vue) to build and customize a new static site.


## Project setup

```bash
npm install
```

### Compiles and hot-reloads for development

```bash
npm run serve
```

### Compiles and minifies for production

```bash
npm run build
```

### Lints and fixes files

```bash
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).


## GitHub Actions Workflows Removed

For security and portability, all GitHub Actions workflows have been removed from this export.  

### What This Means
- `.github/workflows/` folder and all workflow `.yml` files have been deleted.
- Any automated build, test, or deployment scripts tied to the original repository will **not run** in this exported copy.
- This ensures no sensitive organization information, secrets, or deployment keys are included in the export.


## Setting up Environment Variables
This project requires a .env file with environment variables in it. Replace the placeholders with actual configuration details.

Important: Sending emails requires a working email service. Make sure EMAIL_KEY, EMAIL_URL, and other relevant settings point to a valid email provider.
```sh
EMAIL_TO_DEFAULT="sales@g-3chickadee.com" #Use this email as the default email
EMAIL_KEY="YOUR_EMAIL_KEY"
EMAIL_URL="YOUR_EMAIL_URL"
GET_SDS_PASSWORD="YOUR_SDS_PASSWORD" #This was used previously to display SDS on the site, not in use currently but logic remains
GET_SDS_URL="YOU_SDS_URL" #This was used previously to display SDS on the site, not in use currently but logic remains
GET_SDS_USERNAME="YOUR_SDS_USERNAME" #This was used previously to display SDS on the site, not in use currently but logic remains
JWT_ACCESS_SECRET="YOUR_JWT_ACCESS_SECRET"
RECAPTCHA_SECRET="YOUR_RECAPTCHA_SECRET"
```


## Update Site Domain in robots.txt and sitemap.xml

Before deploying this project, the team must update the site domain references in the `robots.txt` and `sitemap.xml` files. These files contain hardcoded, placeholder URLs pointing to `"your-site-domain"`.


### Steps:

1. **Open `robots.txt`**
   - Look for lines like:
     ```
     #https://www.your-site-domain.com/robots.txt
     Sitemap: https://your-site-domain/sitemap.xml
     ```
   - Replace `"your-site-domain"` with your actual production domain.

2. **Open `sitemap.xml`**
   - Look for `<loc>` tags containing `"https://your-site-domain/..."`
   - Replace `"your-site-domain"` with your actual production domain.


## Google Tag Manager (GTM)

The exported project includes placeholder GTM snippets using `GTM-XXXXXXX`. The team must replace these with their own GTM container ID to enable tracking.

### Steps:

1. **Get your GTM container ID**
   - Format: `GTM-XXXXXXX`
   - Obtain this from your Google Tag Manager account.

2. **Replace the placeholder**
   - Open `index.html` and replace all occurrences of `GTM-XXXXXXX` with your actual container ID.

