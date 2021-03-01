# Configuring BlabberJax Content Scheduler With Your Wordpress Website

## System Requirements
1. Ensure you have the latest versions of Wordpress is installed.
2. Validate that your API is functioning properly, by visiting {DOMAIN}.com/wp-json

## BlabberJax Scheduler Setup
1. Install the latest version of the following plugins: 
 - Required:
   - [JWT Auth](https://wordpress.org/plugins/jwt-auth/)
   - [YoastSEO](https://yoast.com/wordpress/plugins/)
 - Optional: 
   - [Custom CSS and JS](https://wordpress.org/plugins/custom-css-js/)
2. Setup a user account for “SSI Design” and send the account information to [client.marketing@blabberjax.com](mailto:client.marketing@blabberjax.com).
 - Note: if you are using [iThemes Security](https://ithemes.com/security/) or other tools, you may need to give this account specific access to Wordpress API endpoints. 
3. Replace the following variables in all [script](/scripts) files:
 - {GA-SITE-VERIFICATION}: The Google Webmaster Tools site verification id sent by your SSI Design representative
 - {INSTANCE-NAME}: The instance name of your BlabberJax scheduler instance
 - {GA-TRACKER-ID}: The Google Analytics classic tracking id send by your SSI Design representative
3. Add the [header code](scripts/header.html) to the header of your website.
    *Recommendation: use [Custom CSS and JS](https://wordpress.org/plugins/custom-css-js/) to ensure this is configured across all pages of your site.*
4. Add this [body code](scripts/body.html) to the end of the body of your website. 
    *Recommendation: use [Custom CSS and JS](https://wordpress.org/plugins/custom-css-js/) to ensure this is configured across all pages of your site.*
5. Identify and send all categories you would like to post articles to by doing the following:
    a. Navigate to https://{domain}.com/wp-json/wp/v2/categories  
    b. Download the response JSON and send it to [client.marketing@blabberjax.com](mailto:client.marketing@blabberjax.com)
6. Once your categories have been configured in your BlabberJax Content Scheduler instance, login and schedule a test post to ensure publishing is working properly!

## CSS & Customization
Feel free to customize the BlabberJax engage form included in each post to match your website's layout.  

To disable BlabberJax engage on your website, set:
```css
.bjx-engage-form, #bjx-engage-lock-by-date-form {
  display: none;
}
```

## Common Issues
1. I can't publish to Wordpress
Typically, this is due to the JWT plugin not being configured correctly.  Be sure to follow the setup guide (here)[https://wordpress.org/plugins/jwt-auth/]
