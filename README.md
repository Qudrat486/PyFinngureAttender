# PyFingureAttender README

## Overview

PyFingureAttender is a Python application that processes attendance logs from `.dat` files and generates `.xlsx` reports. The application provides a graphical user interface (GUI) built using PyQt5, allowing users to browse for attendance log files, process the data, and save the output in a structured Excel format.

## Features

- Browse and select `.dat` files for processing.
- Extract and process attendance data.
- Fill in missing dates with default values.
- Generate and save attendance reports in `.xlsx` format.
- Reset fields and clear outputs.
- User-friendly GUI with PyQt5.

## Prerequisites

- Python 3.x
- Required Python packages:
  - `pandas`
  - `openpyxl`
  - `PyQt5`

Install the required packages using the following command:
```bash
pip install pandas openpyxl PyQt5
```

## Installation

1. Clone or download the repository.
2. Navigate to the directory containing the script.
3. Ensure the required packages are installed.

## Usage

1. Run the script:
   ```bash
   python attendance_log_app.py
   ```
2. The PyFingureAttender GUI will open.
3. Click the `Browse` button to select an attendance log `.dat` file.
4. Click the `Run` button to process the selected file and generate the attendance report.
5. The status and any messages will be displayed in the message box.
6. Click the `Save` button to save the output.
7. Click the `Reset` button to clear the fields and start over.

## GUI Components

- **File Entry**: Displays the selected file path.
- **Browse Button**: Opens a file dialog to select a `.dat` file.
- **Run Button**: Executes the script to process the attendance data.
- **Reset Button**: Clears the file entry and message box.
- **Save Button**: Saves the output to a file.
- **Message Box**: Displays status messages and errors.

## Script Explanation

### `AttendanceLogApp` Class

- **Attributes**:
  - `noFoundIndex`: List to store indexes with no found data.
  - `path`: Path to save the output file.

- **Methods**:
  - `__init__`: Initializes the GUI components.
  - `init_ui`: Sets up the GUI layout and styles.
  - `browse_file`: Opens a file dialog to select a `.dat` file.
  - `reset_fields`: Resets the file entry and message box.
  - `save_output`: Saves the output data to a file.
  - `execute_script`: Processes the attendance log and generates the report.
  - `process_attendance_log`: Filters and processes attendance log data.
  - `extract_date`: Extracts the date and index from the file.
  - `extract_data`: Extracts attendance data from the log.
  - `fill_missing_dates`: Fills missing dates in the data.
  - `find_date_ranges`: Finds date ranges in the data.
  - `create_xlsx`: Creates and saves the Excel report.

### Main Execution

- Defines the `resource_path` function to handle resource paths.
- Initializes the application and shows the GUI.

## License

This project is © 2024 Qudrat Ullah (017-BSCS-21). All rights reserved.

## Author

Qudrat Ullah (017-BSCS-21)