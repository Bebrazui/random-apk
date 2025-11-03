
# Project Blueprint

## Overview

This project demonstrates how to create a bridge between Flutter and web content (HTML/JS) using a WebView. The goal is to build a cross-platform application (Android, iOS, desktop, web) that can render local or remote web pages within a native Flutter shell. This allows for the reuse of existing web assets and combines the power of web technologies with Flutter's native performance and UI capabilities.

## Features & Design

*   **Core:** Flutter application acting as a native container.
*   **WebView Integration:** Uses the `webview_flutter` package to embed web content.
*   **JavaScript Bridge:** Implements a `JavaScriptChannel` to allow communication from the WebView (JavaScript) to the Flutter (Dart) side.
*   **Native Features:** Demonstrates how to access native device features, triggered from the web content. Implemented features include:
    *   Camera permission requests (`permission_handler`)
    *   Local notifications (`flutter_local_notifications`)
    *   Microphone permission requests (`permission_handler`)
    *   Storage access permission requests (`permission_handler`)
    *   Device vibration (`vibration`)
    *   Theme switching (light/dark/system) using `provider`
    *   Get list of installed applications (`device_apps`)
    *   Launch other applications (`device_apps`)
*   **Cross-Platform:** The final application will be buildable for Android, iOS, Windows, macOS, Linux, and Web.
*   **WebAssembly (WASM):** Flutter's web builds compile to WASM, providing near-native performance in the browser.

## Current Plan

1.  **DONE: Add `webview_flutter` dependency.**
2.  **DONE: Implement WebView and load local HTML.**
3.  **DONE: Add `permission_handler`, `flutter_local_notifications`, `vibration` and `device_apps` dependencies.**
4.  **DONE: Configure `AndroidManifest.xml` for `device_apps`.**
5.  **IN PROGRESS: Expand `JavaScriptChannel`:** Add message handlers for app management.
6.  **IN PROGRESS: Update `index.html`:** Add UI for displaying app list and launching apps.
7.  **IN PROGRESS: Implement Native Handlers:** Write Dart code for getting app list and launching apps.
8.  **NEXT: Build and Test:** Verify that all bridge functionalities work as expected.
9.  **FINALLY: Build APK.**
