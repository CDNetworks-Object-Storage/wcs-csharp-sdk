# C# SDK 使用指南

## 1 Brief Introduction

WcsLib is a relatively primitive encapsulation with no JSON library, all correct operations return JSON strings, so you need to choose a JSON library to get it correctly according to the documentations. You might think it not convenient enough, but it has an advantage: you are allowed to choose JSON library yourself. If we use it internally, there are possibilities that are different from what you choose.

We will provide more sample code based on WcsLib and do higher-level encapsulation to solve the convenience problem.

## 2 Version

1.0.1.0

Initial launch, UWP is not supported now, mainly HttpManager class.


## 3 Initialization

Before using the SDK, you need to obtain a valid AccessKey and SecretKey signature authorization.
You can use the following methods:
1. Obtain an account for Object Storage.
2. Log in to the Console portal, view the AccessKey and SecretKey in Security Settings ->  API information management -> AccessKey Management.
3. Log in to the Console portal, view the upload domain (UploadHost) and manage domain (ManageHost)  in Object Storage Service -> Buckets -> Overview -> Domain Names.
Call the following code to initialize after above configurations:

```
Mac mac = new Mac("<AccessKey>", "<SecretKey>");
//Config config = new Config("<UploadHost>", "<ManageHost>", false);	// use HTTP
Config config = new Config("<UploadHost>", "<ManageHost>", true);	// use HTTPS
```

## 4 Instructions

See demo in the test directory in the link of [wcs-csharp-sdk](wcs-csharp-sdk).

![image.png](https://www.wangsu.com/wos/draft/help_doc/en_us/16033/21685/1636080523820_image.png)


