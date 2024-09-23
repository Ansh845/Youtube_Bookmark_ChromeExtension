# Youtube_Bookmark_Extension

Here’s a step-by-step guide to cloning your Chrome extension from GitHub and installing it manually in a user’s Chrome browser.

### 1. **Clone the Extension Repository**
   - **Step 1**: Navigate to your extension’s repository on GitHub.
   - **Step 2**: Click on the **Code** button (the green button located above the file list).
   - **Step 3**: Copy the URL provided under "Clone" (either using HTTPS or SSH).
   - **Step 4**: Open a terminal or command prompt and type the following to clone the repository:

     ```bash
     git clone https://github.com/username/your-extension-repo.git
     ```

     Replace `https://github.com/username/your-extension-repo.git` with the actual URL of your repository. This will download the extension’s code into a local folder on your computer.

### 2. **Prepare the Extension Files**
   - **Step 5**: Navigate to the folder where the extension code was cloned using:

     ```bash
     cd your-extension-repo
     ```

   - **Step 6**: Ensure all necessary files are present (`manifest.json`, `contentScript.js`, any assets like icons). The manifest file is critical for Chrome to recognize the extension.

### 3. **Load the Extension Manually in Chrome**
   - **Step 7**: Open Chrome and go to the Extensions page by typing the following in the address bar:

     ```
     chrome://extensions/
     ```

   - **Step 8**: Enable **Developer Mode**. You’ll find this toggle in the upper right corner of the Extensions page.
   
   - **Step 9**: Click on **Load unpacked**. A file dialog will appear.
   
   - **Step 10**: Navigate to the folder where you cloned the extension and select it. Make sure you’re selecting the root folder containing the `manifest.json` file.

   - **Step 11**: After selecting the folder, Chrome will load the extension. You should see it appear in the list of installed extensions on the Chrome extensions page.

### 4. **Test the Extension**
   - **Step 12**: The extension’s icon should now appear in the Chrome toolbar. Test the extension by performing its intended actions (e.g., running content scripts, interacting with the UI, etc.).

   - **Step 13**: If you make any changes to the code, go back to the `chrome://extensions/` page and click **Reload** under your extension to update it without needing to reinstall.

### 5. **Distribute to Other Users**
   You can share the cloned repository’s URL with other users, and they can follow the same steps to clone and install the extension manually.

### Additional Notes:
- **Ensure Manifest Permissions**: If your extension interacts with websites or uses Chrome APIs, make sure all required permissions are defined in `manifest.json`. For example, adding `"storage"` permission if using `chrome.storage`.

- **Uninstalling the Extension**: Users can remove the extension by navigating to `chrome://extensions/`, finding the extension in the list, and clicking **Remove**.

Following these steps, users will be able to run your extension locally in Chrome without needing to publish it in the Chrome Web Store.
