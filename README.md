# **Yrkus API Shortener**

Contributors: Yrkus  
Version: 1.5  
License: GPL2  
License URI: https://www.gnu.org/licenses/gpl-2.0.html  
A simple, lightweight WordPress plugin that connects to your Yrkus API to generate and save short links for posts and pages.

## **Description**

This plugin integrates your WordPress site directly with the Yrkus URL shortening service. It adds a simple "Generate Yrkus Link" button to your post and page editor, as well as the main post list.

When clicked, it sends the post's permalink to your secure Yrkus API endpoint, gets the short URL back, and saves it to the post's metadata. This makes it incredibly easy to create, save, and copy short links right from your publishing workflow.

## **Features**

* **One-Click Generation:** Generate a Yrkus short link for any post or page from the editor.  
* **Persistent Links:** Your short link is saved to the post, so it's always there when you come back.  
* **Post List Integration:** View, copy, or generate short links directly from the "All Posts" and "All Pages" screens.  
* **Copy to Clipboard:** Automatically copies the new link to your clipboard the moment it's created or when you click the "Copy" button.  
* **Secure API Storage:** Your secret API key is stored securely in the WordPress database.

## **Installation**

You can install this plugin in two ways.

### **1\. WordPress Admin Upload (Easiest)**

1. Download the yrkus-shortener.zip file.  
2. Log in to your WordPress admin dashboard.  
3. Navigate to **Plugins \> Add New**.  
4. Click the **Upload Plugin** button at the top of the page.  
5. Select the yrkus-shortener.zip file you downloaded and click **Install Now**.  
6. Once installed, click **Activate Plugin**.

### **2\. Manual FTP Upload**

1. Unzip the yrkus-shortener.zip file. You will get a folder named yrkus-shortener.  
2. Using an FTP client, upload the entire yrkus-shortener folder to your wp-content/plugins/ directory.  
3. Log in to your WordPress admin dashboard, go to **Plugins**, and find **Yrkus API Shortener** in the list.  
4. Click **Activate**.

## **Configuration**

After activating the plugin, you **must** configure it to connect to your API.

\<\!-- MODIFICATION: Added Step 1 and re-numbered the rest \--\>

1. **Get Your API Key:**  
   * Visit the Yrkus API developer portal at [https://yrkus.com/api/](https://yrkus.com/api/).  
   * Click the "Request an API Key" button and fill out the application form.  
   * Once your request is approved, you will receive your secret API key via email.  
2. **Navigate to Settings:** In your WordPress admin, navigate to **Settings \> Yrkus Shortener**.  
3. **Yrkus API Key:** Paste your secret API key (e.g., sk\_live\_...) into the "Yrkus API Key" field.  
4. **Base API URL:** This field is pre-filled with https://www.yrk.us/api/links. Do not change this unless you are instructed to.  
5. **Save Changes:** Click the "Save Changes" button.

\<\!-- END MODIFICATION \--\>

The plugin is now ready to use\!

## **Usage**

There are two places you can generate and view your short links.

### **1\. In the Post/Page Editor**

When you edit any Post or Page, you will see a new **"Yrkus Short Link"** box in the sidebar (usually on the right).

* **To Generate a Link:** Click the **"Generate Yrkus Link"** button. The plugin will create the link, save it, and display it in the box. The link will also be automatically copied to your clipboard.  
* **To View an Existing Link:** If a link has already been generated for that post, it will be displayed in this box automatically, along with a "Copy" button.

### **2\. In the Post/Page List**

When you navigate to **Posts \> All Posts** or **Pages \> All Pages**, you will see a new column titled **"Yrkus Short Link"**.

* **View/Copy:** If a link exists for a post, it will be displayed in this column with a "Copy" button.  
* **Generate:** If no link exists, a **"Generate Link"** button will appear. You can click this to create the link directly from the list view without having to open the editor.

## **Troubleshooting (FAQ)**

Q: The button shows an error like API Error (Code: 401). Unauthorized...  
A: This means your API Key is incorrect, has been suspended, or was not saved. Go to Settings \> Yrkus Shortener, re-paste your valid API key, and click Save Changes.  
Q: The button shows an error like API Error (Code: 400). Malicious...  
A: Your Yrkus API is configured with Google Safe Browsing. This error means Google has flagged your post's permalink as potentially malicious, and the API has (correctly) refused to create a short link for it.  
Q: The button shows Network Error or API Error (Code: 500).  
A: This means the plugin could not connect to your API server (https://www.yrk.us). This could be a temporary server outage or a firewall on your WordPress server that is blocking outbound cURL requests.
