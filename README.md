# Azure Blob Container Browser

Live demo available on https://kmhuglen.github.io/azureblobcontainerbrowser/

The Azure Blob Container Browser is a web application that allows users to browse and download files from an Azure Blob Storage container. Users need to provide a Shared Access Signature (SAS) URL with read and list permissions. The app lists the blobs (files) in the container, displaying their names, last modified dates, and sizes. Users can click on folders to navigate through the directory structure and download individual files directly from the browser. The app also provides error handling and displays relevant information about CORS and firewall settings required for accessing the storage account.

## Help Guide for Azure Blob Container Browser

### SAS URL Permissions

The SAS (Shared Access Signature) URL you provide must have the necessary permissions to **read** and **list** the blobs in the storage account. Without these permissions, the application will not be able to access or display the blobs.

### CORS Settings

CORS (Cross-Origin Resource Sharing) settings enable your web application to interact with the Azure Blob Storage from a different domain.

To configure CORS settings on your Azure Storage Account in the Azure portal. Navigate to the **Settings** section and select **Resource sharing (CORS)**. Add a new CORS rule with the following details:

- Allowed Origins: https://kmhuglen.github.io
- Allowed Methods: GET
- Allowed Headers: *
- Exposed Headers: *
- Max Age: 200

### Firewall Settings

The firewall settings on your Azure Storage Account must be configured to allow requests from the public IP address of the machine running this application.
        
To configure firewall settings on your Azure Storage Account in the Azure portal. Navigate to the **Security + networking** section and select **Networking**. And ensure either the **Enable from all networks** is selected or that the Public IP address of the machine is added to the Firewall
