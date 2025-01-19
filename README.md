# Syncverse

Syncverse is a Python package that helps you synchronize files between your local storage and cloud storage (Google Drive). With Syncverse, you can easily monitor and keep your files in sync, whether it's uploading, updating, or deleting files on Google Drive or syncing files between local directories.

## Features
- **Local File Sync**: Sync files between two local directories.
- **Google Drive Sync**: Sync files to and from Google Drive, including support for file updates and deletions.
- **Continuous Monitoring**: The package uses `watchdog` to monitor file changes and automatically synchronize them.

## Installation

You can install Syncverse directly from PyPI using `pip`:

```bash
pip install syncverse
