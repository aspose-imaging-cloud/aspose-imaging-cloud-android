# Aspose.Imaging for Cloud Android SDK
[Aspose.Imaging for Cloud](https://products.aspose.cloud/imaging/cloud) is a true REST API that enables you to perform a wide range of image processing operations including creation, manipulation and conversion in the cloud, with zero initial costs. Our Cloud SDKs are wrappers around REST API in various programming languages, allowing you to process images in language of your choice quickly and easily, gaining all benefits of strong types and IDE highlights. 

This repository contains test project and instructions on how to use [Aspose.Imaging for Cloud Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java) for Android. This SDK allows you to work with Aspose.Imaging for Cloud REST APIs in your Android applications quickly and easily, with zero initial cost.

To use this SDK, you will need App SID and App Key which can be looked up at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/#/apps) (free registration in Aspose Cloud is required for this).

The solution uses [Gradle Wrapper](https://github.com/gradle/gradle/tree/master/gradle/wrapper) with no modifications.

# Features
### Image Formats Support
Process options, change and return image in the same format:
* PSD
* JPG
* PNG
* TIFF
* GIF
* BMP
* JPEG2000

Process options, change and return image in the PNG format:
* DICOM
* DNG
* ODG
* EMF
* WMF

### Supported Imaging Operations
* Export to various image formats (currently, all supported formats can be exported to BMP, PSD, JPG, TIFF, GIF, PNG, JPEG2000 or WebP)
* Resize
* Crop
* Rotate and Flip
* TIFF frames extraction
* TIFF frames manipulation
* TIFF concatenation
* TIFF conversion to fax-friendly format
* Retrieve & update image properties
* Conversion to and from PSD format

### Supported Imaging AI Operations
* Content-based image search
* Image duplicates search
* Image search by custom registered tags
* Image comparison and similarity detection
* Image features extraction (for now, AKAZE detector is supported)

# Usage
The project in this repo references [Aspose.Imaging for Cloud Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java) either by placing the binary inside *app/libs* folder with manual handling of transitive dependenices (meant for internal usage only), or by simple addition of the repository dependency with configuring the project accordingly (user scenario) - the behavior is controlled with *CI* environment variable (see [build.gradle](app/build.gradle)).

For the users, the following basic instructions should be applied.

1. Since this library is consuming Aspose.Imaging for Cloud web APIs, please add *INTERNET* permission to your manifest.
```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.your.product.application">
	...
   <uses-permission android:name="android.permission.INTERNET" />
   ...
</manifest>
```
2. Add [Aspose Cloud repository](https://artifact.aspose.cloud).
```gradle
repositories {
    ...
    maven { url 'http://artifact.aspose.cloud/repo/' }
    ...
}
```
3. Add dependency to [Aspose.Imaging for Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java), starting from *18.11* (lower versions may not work).
```gradle
dependencies {
    ...
    implementation group: 'com.aspose', name: 'aspose-imaging-cloud', version: '18.12'
    ...
}
```
4. *Use in case of issues*. Add the following exclusions to get rid of transitive dependencies/classes duplication issues. 
```gradle
configurations.all {
    exclude group: "commons-collections", module: "commons-collections"
    exclude module: "xpp3"
}
```
5. If you also use [Aspose.Storage for Cloud Java SDK](https://github.com/aspose-storage-cloud/aspose-storage-cloud-java) in your project (which is probably the case), please add the following options (in combination with the step proposed above) for it to work on Android. The following config may change with new [Aspose.Storage for Cloud Java SDK](https://github.com/aspose-storage-cloud/aspose-storage-cloud-java) versions to come.
```gradle
android {
    ...
    packagingOptions {
        exclude 'META-INF/jersey-module-version'
    }
}

dependencies {
    ...
    implementation ('com.aspose:aspose-cloud-storage:1.0.1') {
        exclude module: 'xercesImpl'
        exclude module: 'httpcore'
    }
}
```

# Examples
Please, refer to [Aspose.Imaging for Cloud Java SDK](https://github.com/aspose-imaging-cloud/aspose-imaging-cloud-java).

# Tests
Tests are intended for internal usage only with sources be taken from [Aspose.Storage for Cloud Java SDK](https://github.com/aspose-storage-cloud/aspose-storage-cloud-java).

# Licensing
All Aspose.Imaging for Cloud SDKs, helper scripts and templates are licensed under [MIT License](LICENSE).

# Contact Us
Your feedback is very important to us. Please feel free to contact via
+ [**Free Support Forum**](https://forum.aspose.cloud/c/imaging)
+ [**Paid Support Helpdesk**](https://helpdesk.aspose.imaging/)

# Resources
+ [**Web API reference**](https://apireference.aspose.cloud/imaging/)
+ [**Website**](https://www.aspose.cloud)
+ [**Product Home**](https://products.aspose.cloud/imaging/cloud)
+ [**Documentation**](https://docs.aspose.cloud/display/imagingcloud/Home)
+ [**Blog**](https://blog.aspose.cloud/category/aspose-products/aspose.imaging-cloud/)