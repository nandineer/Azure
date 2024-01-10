# Azure

**Create a storage account to host the static website.**

1.	Click + Add to create a new resource.
2.	Search for and select Storage Account.
3.	For Resource Group, select the existing resource group if it is not already selected.
4.	Enter a Storage account name that begins with staticsite. You may need to add some characters at the end of the name to make it unique.
5.	Click Review + Create, then Create.
6.	Configure the storage account for static site hosting.
7.	Wait for your storage account to finish being created. When viewing the resource group, you can click Refresh. When your storage account appears in the list, it has been created.

**Static Website**


8.	Click on your storage account, then click Static Website on the left side of the storage account pane.
9.	Click Enabled to enable static website hosting for the storage account.
10.	For Index document name, enter index.html.
11.	Click Save.
12.	Upload the static site files - through portal or through cloud shell using command

    export AZURE_STORAGE_ACCOUNT=<<storage-account_name>>
    export RESOURCE_GROUP=<<resource_group>>
    az storage account keys list \
      --account-name $AZURE_STORAGE_ACCOUNT \
      --resource-group $RESOURCE_GROUP \
      --output table

     git clone 
   	
     az storage blob upload-batch -s . -d "\$web" --account-name <storage-account-name> --account-key <storage-account-key>

     
14.	In Azure portal, navigate back to the static site storage account and select Static Website again. This page contains a URL under Primary Endpoint. Copy this URL and access it in a new tab.
