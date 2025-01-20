## Syncverse
Syncverse is a Python package that helps you synchronize files between your local storage and cloud storage (Google Drive). With Syncverse, you can easily monitor and keep your files in sync—whether it's uploading, updating, or deleting files on Google Drive, or syncing files between local directories.

## Features
🖥️ Local File Sync - Synchronize files between two local directories.
☁️ Google Drive Sync - Sync files to Google Drive from local, including support for file updates and deletions.

## Installation
Install Syncverse directly from PyPI using:
```pip install syncverse```

## Requirements
Python 3.6 or higher
watchdog for file system monitoring
Google API client libraries for Google Drive integration
To install dependencies manually using requirements.txt: 
```pip install -r requirements.txt```

## Usage
# Importing the Package
```bash
import syncverse
import gdrive_sync
from syncverse.gdrive_sync import GoogleDriveSyncHandler
from syncverse.local_sync import FileSyncHandler```

# Synchronizing Files Locally
Sync files between two local directories:
```from syncverse.local_sync import FileSyncHandler

# Define source and destination file paths
source_file = "path/to/your/sourcefile"
destination_file = "path/to/your/destinationfile"

# Initialize FileSyncHandler
local_sync = FileSyncHandler(source_file, destination_file)

# Start synchronization
local_sync.sync_file() ```






