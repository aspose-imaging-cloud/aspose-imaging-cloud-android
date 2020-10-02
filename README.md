# Aspose.Imaging Cloud Android SDK
[Aspose.Imaging Cloud](https://products.aspose.cloud/imaging) is a true [REST API](https://apireference.aspose.cloud/imaging/) that enables you to perform a wide range of image processing operations including creation, manipulation and conversion in the cloud, with zero initial costs. Our Cloud SDKs are wrappers around REST API in various programming languages, allowing you to process images in language of your choice quickly and easily, gaining all benefits of strong types and IDE highlights. 

This repository contains test project and instructions on how to use [Aspose.Imaging Cloud Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java) for [Android](https://products.aspose.cloud/imaging/android). This SDK allows you to work with Aspose.Imaging Cloud REST APIs in your Android applications quickly and easily, with zero initial cost.

To use this SDK, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (free registration in Aspose Cloud is required for this).

The solution uses [Gradle Wrapper](https://github.com/gradle/gradle/tree/master/gradle/wrapper) with no modifications.

## Key Features
#### Image Formats Support
Export the following images to various formats (generally supported ones are BMP, PSD, JPEG, TIFF, GIF, PNG, JPEG2000, WEBP and PDF):
* BMP
* GIF
* DJVU
* WMF
* EMF
* JPEG
* JPEG2000
* PSD
* TIFF
* WEBP
* PNG
* DICOM
* CDR
* ODG
* OTG
* DNG
* SVG
* CMX

Process options, change and return images in the same format:
* PSD
* JPEG
* TIFF
* GIF
* BMP
* JPEG2000
* WEBP

Process options, change and return images in any supported export format:
* EMF
* WMF

#### Supported Imaging Operations
* Export 
* Resize
* Crop
* Rotate and Flip
* TIFF frames extraction
* TIFF frames manipulation
* TIFF concatenation
* TIFF conversion to fax-friendly format
* Retrieve & update image properties
* Conversion to and from PSD format

#### Supported Imaging AI Operations
* Content-based image search
* Image duplicates search
* Image search by custom registered tags
* Image comparison and similarity detection
* Image features extraction (for now, AKAZE detector is supported)

For the complete list of use-cases, please refer to the [format support document](https://docs.aspose.cloud/imaging/supported-file-formats/) to see what you can achieve!

#### Storage API support
Since version 19.4, SDK includes support of storage operations for better user experience and unification, so now there's no need to use 2 different SDKs!

It gives you an ability to:
* Upload, download, copy, move and delete files, including versions handling (if you are using Cloud storage that supports this feature - true by default)
* Create, copy, move and delete folders
* Copy and move files and folders accross separate storages in scope of a single operation
* Check if certain file, folder or storage exists

Detalied official documentation can be found at the [following link](https://docs.aspose.cloud/imaging/).

## Getting Started
1. **Sign Up**. Before you begin, you need to sign up for an account on our [Dashboard](https://dashboard.aspose.cloud/) and retrieve your [credentials](https://dashboard.aspose.cloud/#/apps).
2. **Minimum requirements**. This SDK requires [Java 1.6 or later](https://java.com/download/).
3. **Add Aspose.Imaging Cloud Java SDK to your project**. The project in this repo references [Aspose.Imaging Cloud Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java) either by placing the binary inside *app/libs* folder with manual handling of transitive dependenices (meant for internal usage only), or by simple addition of the repository dependency with configuring the project accordingly (user scenario) - the behavior is controlled with *CI* environment variable (see [build.gradle](app/build.gradle)). For the users, the following basic instructions should be applied.

Since this library is consuming Aspose.Imaging Cloud web APIs, please add *INTERNET* permission to your manifest.
```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.your.product.application">
	...
   <uses-permission android:name="android.permission.INTERNET" />
   ...
</manifest>
```
Add [Aspose Cloud repository](https://repository.aspose.cloud).
```gradle
repositories {
    ...
    maven { url 'https://repository.aspose.cloud/repo/' }
    ...
}
```
Add dependency to [Aspose.Imaging Cloud Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java), starting from *18.11* (previous versions may not work with Android).
```gradle
dependencies {
    ...
    implementation group: 'com.aspose', name: 'aspose-imaging-cloud', version: '20.9'
    ...
}
```
4. **Using the SDK**. The best way to become familiar with how to use the SDK is to read the [Developer Guide](https://docs.aspose.cloud/imaging/developer-guide/). The [Getting Started Guide](https://docs.aspose.cloud/imaging/getting-started/) will help you to become familiar with the common concepts.

## Quick Examples
Please, refer to [Aspose.Imaging Cloud Java SDK examples](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java#quick-examples).

#### Aspose Cloud-hosted service VS on-premise deployment (*experimental feature*)
Starting from v19.7, you can choose either to use Aspose Cloud-hosted image processing service (the standard way) or the Docker image from Docker Hub deployed on-premise to serve the requests.
The details about key differences and deployment process will be described on the dedicated Docker Hub page as soon as it's released.
To succeed with your on-premise service usage by the SDK, you need to:
1. Use the new API class constructors with either single base URL parameter, or additional API version and debug mode parameters.
```java
ImagingApi imagingApi = new ImagingApi("yourServiceUrl");
```
2. Set *storage* or *storageName* parameters for each request where they're present (mandatory!).

## Content
Please, refer to [Aspose.Imaging Cloud Java SDK content](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java#content).

## Dependencies
* [Java 1.6 or later](https://java.com/download/)

## Licensing
All Aspose.Imaging Cloud SDKs, helper scripts and templates are licensed under [MIT License](LICENSE).

## Contact Us
Your feedback is very important to us. Please feel free to contact via
+ [**Free Support Forum**](https://forum.aspose.cloud/c/imaging)
+ [**Paid Support Helpdesk**](https://helpdesk.aspose.cloud/)

## Resources
+ [**Web API reference**](https://apireference.aspose.cloud/imaging/)
+ [**Website**](https://www.aspose.cloud)
+ [**Product Home**](https://products.aspose.cloud/imaging)
+ [**Documentation**](https://docs.aspose.cloud/imaging/)
+ [**Blog**](https://blog.aspose.cloud/category/imaging/)

## Other languages
We generate our SDKs in different languages so you may check if yours is available in our [repository](https://github.com/aspose-imaging-cloud). If you don't find your language in the list, feel free to request it from us, or use raw REST API requests as you can find it [here](https://products.aspose.cloud/imaging/curl).

## Code generator
The solution is updated using [code generator](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-codegen).
