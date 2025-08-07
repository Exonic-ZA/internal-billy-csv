# Timesheet Data Preparation Tool

A simple web-based tool for processing timesheet CSV files by adding month and year columns. This tool allows data analysts to easily add temporal context to timesheet data for batch processing and analysis.

## Overview

The Timesheet Data Preparation Tool is designed to streamline the process of preparing timesheet data for analysis. It takes CSV files containing timesheet data and adds month and year columns based on a user-specified date range, making it easy to concatenate multiple files and perform time-based analysis.

## Features

- **Single HTML File**: Self-contained tool requiring no server setup or external dependencies
- **CSV File Upload**: Support for standard CSV files with timesheet data
- **Date Range Input**: Add month and year columns based on specified date range
- **Data Preview**: View processed data before downloading
- **Automatic Download**: Generate processed files with standardized naming
- **Client-Side Processing**: All data processing happens locally for privacy and security

## Usage

### Getting Started

1. Open `index.html` in any modern web browser
2. The tool will display a clean, intuitive interface

### Processing Timesheet Data

1. **Upload CSV File**:
   - Click "Choose File" to select your timesheet CSV
   - Supported format: CSV files with columns "Tracked by Name", "Billable", and "Sum"

2. **Set Date Range**:
   - Select the start and end dates for the timesheet period
   - The tool will extract month and year from your date selection

3. **Process Data**:
   - Click "Process Data" to add month and year columns
   - A preview of the processed data will appear

4. **Download Results**:
   - Click "Download Processed CSV" to save the enhanced file
   - File will be named `<original_filename>_processed.csv`

### Expected Input Format

Your CSV file should contain the following columns:
```
Tracked by Name,Billable,Sum
John Doe,Yes,45.5
Jane Smith,No,32.25
```

### Output Format

The processed file will include the original data plus month and year columns:
```
Tracked by Name,Billable,Sum,Month,Year
John Doe,Yes,45.5,January,2024
Jane Smith,No,32.25,January,2024
```

## Sample Data

The `data/` directory contains sample CSV files:
- `data.csv`: Sample timesheet data for testing
- `data-rands.csv`: Additional sample data

## Technical Details

- **Technology**: Pure HTML, CSS, and JavaScript
- **Dependencies**: None (completely self-contained)
- **Browser Support**: Modern browsers (Chrome, Firefox, Safari, Edge)
- **Processing**: Client-side only (no data leaves your browser)

## File Structure

```
├── index.html          # Main application file
├── data/              # Sample data files
│   ├── data.csv       # Sample timesheet data
│   └── data-rands.csv # Additional sample data
├── .kiro/             # Project specifications
└── test/              # API documentation and test files
```

## Privacy & Security

- All data processing occurs client-side in your browser
- No data is transmitted to external servers
- Files are processed locally and remain on your machine
- No tracking or analytics implemented

## Requirements Met

This tool satisfies the following requirements:
- ✅ Upload CSV files with date range specification
- ✅ Process timesheet data by adding month and year columns
- ✅ Download processed data with standardized filenames
- ✅ Preview processed data before download
- ✅ Single HTML file deployment
- ✅ Client-side processing for security

## License

Internal tool for Billy's data processing needs.