# Google Takeout Timestamp Fixer

## Overview

If you've ever used Google Takeout to download your photos and videos, you may have noticed that the original photo/video files are separated from the accompanying metadata (in JSON format). This script helps you automatically update the **creation timestamp** of your photos and videos with the correct time from the associated JSON file.

### Problem:

- Google Takeout separates photos/videos and their metadata (JSON files).
- The file metadata includes the actual **"photo taken time"**, but this information isn't reflected in the file's timestamp.

### Solution:

This script will:

- Read the JSON file.
- Extract the correct **photo taken time** from the metadata.
- Update the **file's last modified and access time** with that timestamp.

This is especially useful for users who want to keep their photos and videos organized by date but are unable to easily do so after extracting files from Google Takeout.

---

## How to Use:

### Prerequisites:

- **Python** must be installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
- Basic knowledge of using the command line.

### Steps:

1. Download the `google-takeout-timestamp-fixer` repository.
2. Place the extracted Google Takeout folder in the same directory as the script.
3. Update the `directory_path` variable in the script to point to your Google Takeout folder:
   - Open the script file (`date_modifier_script.py`) in any text editor.
   - Update the `directory_path` variable with the path to your Google Takeout folder.

Example:

```python
directory_path = r"C:\Users\YourName\Google Photos Downloads"
```

4. Open a command prompt or terminal.
5. Navigate to the folder where the script is located.
6. Run the script with the following command:

```python
google_takeout_timestamp_fixer.py
```

The script will process all .json files in the specified directory, extract the "photo taken time" from the JSON, and update the corresponding photo/video file with the correct timestamp.

### Additional Information:

- The script will look for .json files and their associated photo/video files (same name, .jpg, .mp4, etc.).
- The photoTakenTime in the JSON file is used to update the file's last modified timestamp.

### Troubleshooting:

- Ensure your Google Takeout files are organized with .json files and their corresponding media files in the same folder.
- If you encounter any issues with file paths, make sure the directory_path variable is set correctly.

### License:

This project is licensed under the MIT License - see the LICENSE file for details.
