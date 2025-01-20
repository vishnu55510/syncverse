# Syncverse

Syncverse is a Python package that helps you synchronize files between your local storage and cloud storage (Google Drive). With Syncverse, you can easily monitor and keep your files in sync, whether it's uploading, updating, or deleting files on Google Drive or syncing files between local directories.

## Features
- **Local File Sync**: Sync files between two local directories.
- **Google Drive Sync**: Sync files to and from Google Drive, including support for file updates and deletions.

## Installation

You can install Syncverse directly from PyPI using `pip`:


`pip install syncverse`


## Requirements
Python 3.6 or higher
watchdog for file system monitoring
Google API client libraries for Google Drive integration

You can also install the dependencies manually via the requirements.txt:

`pip install -r requirements.txt`


## Usage

1. Importing the Package
You can import the package and the required modules as follows:
```import syncverse
from syncverse.gdrive_sync import GoogleDriveSyncHandler
from syncverse.local_sync import FileSyncHandler```

2. Synchronizing Files Locally
To synchronize files between two local directories, use:
```from syncverse.local_sync import FileSyncHandler

# Define source and destination file paths
source_file = "path to your sourcefile"
destination_file = "path to your deatinationfile"

# Initialize FileSyncHandler
local_sync = FileSyncHandler(source_file, destination_file)

# Start synchronization
local_sync.sync_file() ```

Explanation:

```FileSyncHandler```: Monitors and synchronizes changes from a source file to a destination file.

3. Synchronizing Files with Google Drive
To synchronize a local file with Google Drive, follow these steps:
```from syncverse.gdrive_sync import GoogleDriveSyncHandler
from syncverse.gdrive_sync import authenticate_drive```.

# Authenticate Google Drive
drive_service = authenticate_drive() #Set your google credentials.json in working directorie

# Define local file path
local_file_path = "path to your localfile"

# Initialize GoogleDriveSyncHandler
drive = GoogleDriveSyncHandler(local_file_path, drive_service, file_id=None)

#Start synchronization
drive.sync_to_drive()```

## Explanation:

authenticate_drive(): Authenticates and connects to Google Drive.
GoogleDriveSyncHandler: Handles synchronization between the local file and Google Drive.
file_id: If set to None, a new file will be uploaded; if an ID is provided, the file will be updated instead.

## Authentication (Google Drive)
For Google Drive synchronization, you’ll need to authenticate your Google account. The first time you run a Google Drive sync, the package will prompt you to authenticate using OAuth2. After successful authentication, your credentials will be stored in a token.json file, so you don't need to authenticate again.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
This package uses the watchdog library for monitoring file system events.
Google API Client Library for Python (google-api-python-client) is used to interact with Google Drive.
