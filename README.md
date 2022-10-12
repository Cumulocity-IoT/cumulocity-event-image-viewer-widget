
# Cumulocity Widget - Event Image Viewer Widget[<img width="35" src="https://user-images.githubusercontent.com/67993842/97668428-f360cc80-1aa7-11eb-8801-da578bda4334.png"/>](https://github.com/SoftwareAG/cumulocity-event-image-viewer-widget/releases/download/2.0.0/event-image-viewer-runtime-widget-2.0.0.zip)

This is an Angular widget designed to display the events that are created whenever the image is captured by the camera device which in turn triggers the webm.io workflow and the captured image which is stored in AWS S3 or any other storage medium is displayed in the widget. The image is classified good or bad based on AI Predictive analytics. 

### Please choose Event Image Viewer Widget release based on Cumulocity/Application builder version:

|APPLICATION BUILDER | CUMULOCITY | EVENT IMAGE VIEWER WIDGET |
|--------------------|------------|---------------------------|
| 1.3.x              | >= 1011.x.x| 2.x.x                     |
| 1.2.x              | 1010.x.x   | 1.x.x                     |  



![s3_image_viewer_widget](https://user-images.githubusercontent.com/70568133/102998337-fe3a5980-454c-11eb-8fee-51ad96c5c927.PNG)

## Features

 *  **Displays the events.**
 *  **Displays the captured images.** 
 * **Uses AI Predictive analytics for image classification** 
 
## Installation
## Runtime Widget Installation (Without Application Deployment)

* This widget support runtime deployment. Download [Runtime Binary](https://github.com/SoftwareAG/cumulocity-event-image-viewer-widget/releases/download/2.0.0/event-image-viewer-runtime-widget-2.0.0.zip) and use application builder to install your runtime widget.

  
**Supported Cumulocity Environments:**
  
 -  **App Builder:**  Tested with Cumulocity App Builder version 1.3.0

**Prerequisites:**
  
* Git
  
* NodeJS (release builds are currently built with  `v14.18.0`)
  
* NPM (Included with NodeJS)

**External dependencies:**

```
"@angular/material": "^11.1.2"

"@ng-select/ng-select": "^6.1.0"
```

**Installation Steps For App Builder:**

**Note:** If you are new to App Builder or not yet downloaded/clone app builder code then please follow [App builder documentation(Build Instructions)](https://github.com/SoftwareAG/cumulocity-app-builder) before proceeding further.

1. Open Your existing App Builder project and install external dependencies by executing below command or install it manually.
   
   npm i @angular/material@11.1.2 @ng-select/ng-select@6.1.0


2. Grab the Event Image Viewer Widget **[Latest Release Binary](https://github.com/SoftwareAG/cumulocity-event-image-viewer-widget/releases/download/2.0.0/gp-event-image-viewer-2.0.0.tgz)**

3. Install the Binary file in app builder.

```
npm i <binary  file  path>/gp-event-image-viewer-2.0.0.tgz
```
4. Open index.less located at /cumulocity-app-builder/ui-assets/

5. Update index.less file with below theme. Import at first line in file/beginning of file(Please ignore this step if it already exist).

```
@import '~@angular/material/prebuilt-themes/indigo-pink.css';
@import '~@c8y/style/main.less';
@import '~@c8y/style/extend.less';
```
6. Import GpEventImageViewerModule in app.module.ts and also place the imported Module under `@NgModule`.

```

import {GpEventImageViewerModule} from 'gp-event-image-viewer';

@NgModule({

  imports: [

    GpEventImageViewerModule    

      ]

  })

```

7.  Congratulation! Installation is now completed. Now you can run app builder locally or build and deploy it into your tenant.
  
```
//Start App Builder
npm run start
// Build App
npm run build
// Deploy App
npm run deploy
```



## Build Instructions
  
**Note:** It is only necessary to follow these instructions if you are modifying/extending this widget, otherwise see the [Installation Guide](#Installation).
  
**Prerequisites:**
  
* Git
  
* NodeJS (release builds are currently built with `v14.18.0`)
  
* NPM (Included with NodeJS)

**Instructions**

1. Clone the repository:
```
git clone https://github.com/SoftwareAG/cumulocity-event-image-viewer-widget.git
```
2. Change directory:

  ```cd s3-image-viewer```

3. run npm i command to install all library files specified in source code

  ```npm i ``` 

4. run npm run buildMinor command to create a binary file under dist folder

  ```npm run buildMinor ``` 

5. (Optional) Local development server:
  
  ```npm start```

6. Build the app:

  ```npm run build```

7. Deploy the app:
  ```npm run deploy```

## QuickStart
This guide will teach you how to add widget in your existing or new dashboard.

1. Open the Application Builder from the app switcher (Next to your username in the top right)

2. Click Add application

3. Enter the application details and click Save

4. Select Add dashboard

5. Click Blank Dashboard

6. Enter the dashboard details and click Save

7. Select the dashboard from the navigation

8. Check for your widget and test it out.

Congratulations! Event Image Viewer Widget is configured.
  
## User Guide

1. Target Assets/Devices - select group of interest
![s3_image_viewer_config1](https://user-images.githubusercontent.com/70568133/102999005-473edd80-454e-11eb-9a09-9bb6aac913a4.PNG)
![s3_image_viewer_config2](https://user-images.githubusercontent.com/70568133/102999029-50c84580-454e-11eb-8787-236fcc998985.PNG)

## Troubleshooting
  
This widget is provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
  
_____________________
  
For more information you can Ask a Question in the [TECHcommunity Forums](https://tech.forums.softwareag.com/tags/c/forum/1/Cumulocity-IoT).
  
  
You can find additional information in the [Software AG TECHcommunity](https://tech.forums.softwareag.com/tag/Cumulocity-IoT).
