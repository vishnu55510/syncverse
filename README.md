# Syncverse

Syncverse is a Python package that helps you synchronize files between your local storage and cloud storage (Google Drive). With Syncverse, you can easily monitor and keep your files in sync, whether it's uploading, updating, or deleting files on Google Drive or syncing files between local directories.

## Features
- **Local File Sync**: Sync files between two local directories.
- **Google Drive Sync**: Sync files to and from Google Drive, including support for file updates and deletions.
- **Continuous Monitoring**: The package uses `watchdog` to monitor file changes and automatically synchronize them.

## Installation

You can install Syncverse directly from PyPI using `pip`:


`pip install syncverse`


## Requirements
Python 3.6 or higher
watchdog for file system monitoring
Google API client libraries for Google Drive integration

You can also install the dependencies manually via the requirements.txt:

`pip install -r requirements.txt`

## Authentication (Google Drive)
For Google Drive synchronization, you’ll need to authenticate your Google account. The first time you run a Google Drive sync, the package will prompt you to authenticate using OAuth2. After successful authentication, your credentials will be stored in a token.json file, so you don't need to authenticate again.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
This package uses the watchdog library for monitoring file system events.
Google API Client Library for Python (google-api-python-client) is used to interact with Google Drive.
