# JARVIS Personal AI Assistant

JARVIS is a Python-based personal AI assistant that can perform various tasks like playing music, opening applications, fetching information from Wikipedia, reading books, automating tasks in Chrome and YouTube, and much more.

Install necessary dependencies using:
pip install -r requirements.txt

## Features

- **Voice Interaction:** Communicate with JARVIS using voice commands.
- **Music Player:** Play songs from local storage and YouTube.
- **Web Interaction:** Open websites like YouTube, Facebook, Instagram, etc.
- **Information Retrieval:** Fetch information from Wikipedia, perform Google searches, and fetch temperature information.
- **Book Reading:** Read PDF books aloud and translate text.
- **Task Automation:** Automate tasks in Chrome, YouTube, and other applications.
- **Reminder:** Remember user inputs and recall them when requested.



## Customizing Application Paths

By default, JARVIS uses specific paths to launch applications like VS Code, Telegram, Chrome, etc. These paths may need to be customized based on your local system configuration.

### Steps to Customize Paths:

1. **Identify Application Paths:**
   Open the `jarvis.py` file and locate the `OpenApps()` function. In this function, you will find conditional statements like `if 'code' in query:`, `if 'telegram' in query:`, etc.

2. **Modify Path Variables:**
   Replace the existing paths with the paths specific to your system. For example:
   - If you have VS Code installed in a different directory, update the path in `os.startfile()` accordingly:
     ```python
     os.startfile("E:\\Applications\\Microsoft VS Code\\Code.exe")
     ```
   - Update paths for other applications like Telegram, Chrome, etc., similarly.

3. **Save Changes:**
   After making the necessary modifications, save the `jarvis.py` file.

4. **Run the Application:**
   Follow the setup instructions provided earlier in the README to run JARVIS. Ensure that the Python environment and dependencies are correctly set up.

5. **Test the Customization:**
   Once JARVIS is running, test the application launch commands by giving voice commands like "Open VS Code", "Open Telegram", etc., and verify that the correct applications are launched.

### Example:

If your VS Code is installed in `C:\Program Files\VS Code\Code.exe`, the corresponding line in `OpenApps()` function should be updated as:
```python
if 'code' in query:
    os.startfile("C:\\Program Files\\VS Code\\Code.exe")
