# Process Hollower

A small Windows research tool for learning how process hollowing works at a low level.

This project demonstrates a technique that:
* Creates a suspended process.
* Replaces its memory with another executable.
* Fixes the thread context.
* Resumes execution so the new code runs inside the original process shell.

Built for reverse engineering practice, Windows internals study, and defensive research.

## ✨ Features

* Creates a target process in suspended mode.
* Unmaps the original image from memory.
* Injects a new PE (Portable Executable) image into the process.
* Fixes the entry point and thread context.
* Resumes execution with the injected code.

## 🚀 Usage

1. Build the project in Visual Studio using the **Release x64** configuration.
2. Run the tool from an elevated command prompt (Administrator) with the following syntax:

    ```bash
    ProcessHollower.exe host.exe payload.exe
    ```

    **Parameters:**
    * `host.exe`: The legitimate process that will act as the shell.
    * `payload.exe`: The executable that will be injected and run.

### 📖 Example

```bash
ProcessHollower.exe notepad.exe demo.exe
<img width="1024" height="1024" alt="qwdqwdqd" src="https://github.com/user-attachments/assets/0d7807a0-08bc-46c1-97bd-b71904d9c58b" />

