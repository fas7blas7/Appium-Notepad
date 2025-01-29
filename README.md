# Appium-Notepad

This repository contains automated tests for a Notepad application using Appium with C#.

## Prerequisites

- .NET Core SDK
- Appium server
- Android Emulator or a physical Android device
- Notepad APK file

## Setup

1. **Clone the repository:**
    ```bash
    git clone https://github.com/fas7blas7/Appium-Notepad.git
    cd Appium-Notepad
    ```

2. **Install Appium:**
    Follow the instructions on [Appium's official website](http://appium.io/) to install Appium.

3. **Start the Appium server:**
    ```bash
    appium
    ```

4. **Configure the Android Emulator:**
    Ensure you have an Android Emulator set up with the name `Pixel_7` or modify the `DeviceName` in the `Setup` method in `PomTests.cs` to match your emulator/device name.

5. **Place the Notepad APK:**
    Ensure the Notepad APK is located at `D:\Notepad.apk` or modify the `App` path in the `Setup` method to match the location of your APK.

## Running the Tests

1. **Navigate to the test project directory:**
    ```bash
    cd NotepadTestsPom
    ```

2. **Run the tests using the .NET CLI:**
    ```bash
    dotnet test
    ```

## Test Cases

### 1. Create Note
- Adds a new note with the content "Test_1".
- Verifies the note is created successfully with the correct content.

### 2. Edit Note
- Adds a new note with the content "Test_2".
- Edits the note content to "Edited".
- Verifies the note content is updated successfully.

### 3. Delete Note
- Adds a new note with the content "Note for Delete".
- Deletes the note.
- Verifies the note is deleted successfully.

## Notes

- The Appium server and the Android Emulator should be running before executing the tests.
- The `AppiumLocalService` is commented out in the code. Uncomment it if you need to start the Appium server programmatically.
