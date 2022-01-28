# C# SDK User Guide

## 1 Initialization

**AK/SK**, **Upload Domain** and **Manage Domain** is required for C# SDK. You can get these information by following steps:
1. account: Apply for CDNetworks cloud storage service, get the account.

2. AK/SK: Log in to CDNetworks SI portal, and you can get the AccessKey and SecretKey in Security Console - AK/SK Management

3. puturl&mgrurl: Log in to SI portal and view the Upload Domain (puturl) and Manage Domain (mgrurl) in Bucket Overview -> Bucket Settings

Initialize after getting these information:
```
Mac mac = new Mac("<AccessKey>", "<SecretKey>");
//Config config = new Config("<UploadHost>", "<ManageHost>", false);	// by HTTP
Config config = new Config("<UploadHost>", "<ManageHost>", true);	// by HTTPS
```

## 2 How to use

See demo under test directory.


