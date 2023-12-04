# ci_cd_fastlane

Setup CI-CD with gitLab or gitHub and Fastlane.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

# Doc support CI-CD: https://blog.codemagic.io/deploying-flutter-app-to-firebase-app-distribution-using-fastlane/

# Cấu hình Fastlane + Firebase App Distribution.

## Install Firebase CLI

1. For installing Firebase CLI, just run the following command from the terminal: curl
   -sL https://firebase.tools | bash
2. Then log in to Firebase to get access to your Firebase projects: firebase login

## Install fastlane

1. To install fastlane using RubyGems, just run this command from the terminal: sudo gem install
   fastlane -NV
2. Alternatively, you can also use this command to install it using Homebrew: brew install fastlane

## Set up fastlane for Android

Terminal: fastlane init

## Add the Firebase App Distribution plugin

Terminal: fastlane add_plugin firebase_app_distribution

## Creating a Firebase project

1. Go to the https://console.firebase.google.com/.
2. Click on Add project.
3. Add a name of the project and click on Continue.
4. Go to Settings –> Project settings.
5. Now, enter the Support email and the GCP resource location.

## Adding Android project

1. Scroll down and click on the Android icon to add your Android project.
2. Enter the Android package name, App nickname and SHA-1, then click on Register app.
3. Download the google-services.json file and place it in the desired folder, then click on Next.
4. Add the Firebase SDK as per the instruction.
5. Click on Continue to console.

## Customizing the Android Fastfile

## Deploying to Firebase App Distribution

Check project đa có trong firebase hay chưa: firebase projects:list

## Deploying Android app

1. Với build android:
   Terminal: fastlane android <lane_name>
   Ex: fastlane android android_release

----------------------------------------------------------------------------------------------------

# Cấu hình thông báo slack khi build app thành công lên App Distribution.

# Tạo webhooks slack:

Step 1: Tạo project slack.
Step 2: Tạo channel.
Step 3: Chon channel muốn đẩy thông báo tự động
=> ấn chuột phải
=> chọn "View channel details"
=> chọn tab "Integrations"
=> chọn "App" và ấn vào nút "Add an app"
=> search với key "incoming webhooks"
=> chọn "Install"
=> chọn "Add to slack"
=> Tại "Post to Channel" chọn "Choose a channel..." chọn channel muốn đẩy thông báo và ấn "Add
Incoming Webhooks Integration",
=> Copy link webhooks và dùng nó thôi.