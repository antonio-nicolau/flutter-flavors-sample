# Flutter Flavors Sample Project

This Flutter project serves as a simple example to demonstrate the concept of "flavors" in Flutter applications. Flavors allow you to create multiple variations of your app with different configurations, resources, and behavior, catering to various environments or purposes.


## What are Flavors?

In Flutter, "flavors" refer to the ability to create different variations of your app based on different configurations. This allows you to manage environments, such as development, staging, and production, or create custom versions for different clients.

In this project, we'll explore how to set up flavors for both Android and iOS platforms.

## Project Overview

This sample Flutter project is a basic application that showcases the use of flavors. It includes three flavors: `development`, `staging`, and `production`. Each flavor has its own configuration, such as different app names,firebase configuration.

## Getting Started

### Configuration

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/flutter-flavors-sample.git
   cd flutter-flavors-sample

2. Running the App
To run the app with a specific flavor, use the following command:

``` bach
flutter run -t <target_main_file> --flavor <flavor_name>
```

## Configure Firebase for Different Flavors

If you want to use different Firebase projects for each environment (flavor), follow these steps:

1. **Create Firebase Projects:**

   Create separate Firebase projects for each environment (development, staging, production) on the [Firebase Console](https://console.firebase.google.com/).

2. **Download Google-services.json:**

   Download the `google-services.json` file for each Firebase project from the Firebase Console.

3. **Place Google-services.json into Correspondent Flavor:**

   For each flavor, place the corresponding `google-services.json` file into the respective flavor directory under `app/src`. Create separate directories for each flavor:
     - app/src/development
     - app/src/staging
     - app/src/production

This code snippet assumes that you have flavors named development, staging, and production. Adjust the names accordingly based on your flavor names.

## Build and Deploy

When building the app for different flavors, you can use the following commands:

Build for development flavor:
``` bash
flutter build <platform> -t lib/main_development.dart --flavor development
```

Build for staging flavor:
``` bash
flutter build <platform> -t lib/main_staging.dart --flavor staging
```
Build for production flavor:
``` bash
flutter build <platform> -t lib/main.dart --flavor production
```
Replace <platform> with either appbundle for Android or ios for iOS.
