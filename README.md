# NewsNow 

NewsNow is an Android application that provides seamless in-app browsing.
## Features & Implementation

### 1. Navigation Drawer
- Implements a **Navigation Drawer** for seamless app navigation.
- Uses `android:menuCategory="secondary"` to manage **back stack behavior** efficiently.

### 2. WebView Integration
- Uses **WebView** to access the website directly within the app.
- Ensure **Internet Permission** is added in `AndroidManifest.xml`:
  
  ```xml
  <uses-permission android:name="android.permission.INTERNET" />
  ```
  
- Reference: [Adding Internet Permission](https://java2blog.com/add-internet-permission-in-androidmanifest-android-studio/)

### 3. WebView Controller
- Ensures that all user interactions on the WebView happen **within the app** and not in an external browser.
- Override URL loading in WebView using:
  
  ```java
  public boolean shouldOverrideUrlLoading(WebView view, String url) {
      view.loadUrl(url);
      return true;
  }
  ```

### 4. ViewModel Cleanup
- The **ViewModel** can be removed as the `TextView` is no longer used in the project.

## How to View the Animations
Below is the demo video:

<a href="https://github.com/user-attachments/assets/5525dadd-7af8-4551-a2b6-02c7dae254f4"
  alt="Watch the video">
</a>
