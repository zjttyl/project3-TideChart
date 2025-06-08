# GYYKS Tide Chart (BugBash Release)

## Overview
The GYYKS Tide Chart is a browser-based HTML application that displays tide predictions for multiple U.S. locations, built by GYYKS. This BugBash release (v1.1) fetches tide data from NOAA’s API and presents it in a table (time, height in feet, type) and a Chart.js graph (tide heights over time). It supports custom date ranges and multiple locations, with a minimalist interface.

### Release Details
- **Version**: v1.1-bugbash
- **Release Date**: June 2, 2025
- **GitHub Release**: [v1.1-bugbash](https://github.com/zjttyl/project3-TideChart/releases/tag/v1.1-bugbash)
- **Purpose**: Prepared for the CSS 360 BugBash event, for classmates to test and report issues using the `BugBash` label in the GitHub issue tracker.

## Features
- **Default Tide Display**: Shows today's tide predictions of Seattle for initial view of the site.
- **Tide Data Display**: Shows tide histories and predictions (time, height in feet, high/low type) for a selected date range and location in a table and Chart.js graph.
- **Location Selection**: Supports six locations via dropdown: Seattle, Los Angeles, Anchorage, New York, Miami, and Bremerton.
- **Custom Date Selection**: Includes start/end date pickers (defaulting to today, June 2, 2025) for single-day or multi-day tide data.
- **Preset Buttons**: Quick selection for Today, Past Week, Next Week, Past Month, and Next Month date ranges.
- **Error Handling**: Displays an alert if the NOAA API fails to load data.
- **Performance**: Loads in under 2 seconds and supports up to 100 concurrent users.
- **Recent Fixes**: Corrected table and chart labels from "Height (m)" to "Height (feet)" to match NOAA API units=english.

## How to Run
The application is browser-based and runs in Google Chrome without additional software.

1. **Access via GitHub Pages (Recommended for BugBash)**:
   - Open [https://zjttyl.github.io/project3-TideChart/](https://zjttyl.github.io/project3-TideChart/) in Google Chrome.
   - No setup or server required; the application loads directly with NOAA API access.

2. **Alternative: Run Locally**:
   - **Clone or Download Repository**:
     ```bash
     git clone https://github.com/zjttyl/project3-TideChart.git
     cd project3-TideChart
     ```
     Or download the zip from the [GitHub release page](https://github.com/zjttyl/project3-TideChart/releases/tag/v1.1-bugbash).
   - **Verify Directory Structure**:
     Ensure the following files are present:
     ```
     .
     ├── docs
     │   └── git-guide.md
     ├── image
     │   ├── background.jpg
     │   └── tide1.gif
     ├── index.html
     └── README.md
     ```
   - **Start a Local Server** (recommended for local testing):
     ```bash
     python -m http.server
     ```
     Or, if Python 3 is installed:
     ```bash
     python3 -m http.server
     ```
   - **Open in Chrome**:
     Navigate to `http://localhost:8000` in Google Chrome. Alternatively, double-click `index.html` (note: some browsers may restrict API calls without a server).

3. **Usage Instructions**:
   - Select a location from the dropdown (e.g., Seattle).
   - Choose a date range using the Start Date and End Date pickers or preset buttons (Today, Past Week, etc.).
   - Click "Get Tides" to fetch and display tide data.
   - View the tide table and graph; scroll down for tide information and animation.

4. **System Requirements**:
   - Google Chrome (latest version recommended).
   - Internet connection for NOAA API access.
   - No additional software (e.g., JDK, Python) required beyond a browser.

## BugBash Instructions
- **Event**: in-class BugBash.
- **Testing**: Use the application in Chrome, trying various locations, date ranges, and edge cases (e.g., invalid dates, rapid clicks).
- **Reporting Issues**:
  - File issues at [https://github.com/zjttyl/project3-TideChart/issues](https://github.com/zjttyl/project3-TideChart/issues).
  - Use the `BugBash` label.
  - Include steps to reproduce, expected behavior, and actual behavior.

## Version Control
- **Branch**: `v1.1`
- **Tag**: `v1.1-bugbash`.

