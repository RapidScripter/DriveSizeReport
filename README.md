# DriveSizeReport - PowerShell Script to Calculate Folder Sizes

## Description

This PowerShell script scans a specified directory and recursively calculates the size of all folders and subfolders. The results are displayed in the console and exported to a CSV file for further analysis. This script helps users quickly identify large folders and manage disk space efficiently.

## Parameters

- `$path` - Specifies the root directory to scan. Default: `"C:\"`
- `$outputFile` - Specifies the CSV file where the folder size report will be saved. Default: `"C:\FolderSize.csv"`

## Prerequisites

1. **Windows PowerShell (5.1 or later)**
2. **Administrator permissions** (recommended for full access to all folders)
3. **Sufficient disk space** for generating large reports

## Installation & Usage

1. Clone or Download the Script
   ```bash
   git clone https://github.com/RapidScripter/DriveSizeReport.git

2. Open PowerShell with Administrator Privileges

3. Modify Parameters if Needed
- Open the script in a text editor and update the following variables as needed:
  ```powershell
  $path = "C:\"  # Change this to your target directory
  $outputFile = "C:\FolderSize.csv"  # Change this to your preferred output path

4. Run the Script
- Execute the script by running:
  ```powershell
  .\DriveSize.ps1

5. View the Output
- The folder sizes will be displayed in the console.
- A CSV report will be generated at the specified `$outputFile` location.

## Script Details

1. Retrieve Folder List
- Uses `Get-ChildItem` to get all folders and subfolders recursively.

2. Calculate Folder Size
- Iterates through each folder and sums the file sizes using `Measure-Object`.

3. Export the Data
- Displays the result in a formatted table.
- Exports the data to a CSV file for further analysis.

## Notes
- Large directories may take longer to process.
- Ensure that PowerShell has the necessary permissions to access all directories.
- Modify `$path` and `$outputFile` to customize the scan location and output path.
