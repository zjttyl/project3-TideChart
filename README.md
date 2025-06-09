# GYYKS Tide Chart (Final Release)

## Overview
The GYYKS Tide Chart is a web-based application that provides tide predictions for six U.S. locations (Seattle, Los Angeles, Anchorage, New York, Miami, Bremerton) using the NOAA API. Users can select date ranges (Today, Past Week, Next Week, Past Month, Next Month) or custom dates to view tide heights in a table and graph with a minimalist interface. The project expands location abd flexible date selection.

### Release Details
- **Version**: v1.3.0
- **Release Date**: June 8, 2025
- **GitHub Release**: [v1.3.0](https://github.com/zjttyl/project3-TideChart/releases/tag/v1.3.0)
- **Purpose**: GYYKS final release for CSS 360 project-3.

## Functionality list
- **Default Tide Display**: Shows today's tide predictions of Seattle for initial view of the site.
- **Tide Data Display**: Shows tide histories and predictions (time, height in feet, high/low type) for a selected date range and location in a table and Chart.js graph.
- **Location Selection**: Supports six locations via dropdown: Seattle, Los Angeles, Anchorage, New York, Miami, and Bremerton.
- **Custom Date Selection**: Includes start/end date pickers (defaulting to today, June 2, 2025) for single-day or multi-day tide data.
- **Preset Buttons**: Quick selection for Today, Past Week, Next Week, Past Month, and Next Month date ranges.
- **UI**: Clean and minimalistic UI design
- **Error Handling**: Displays an alert if the NOAA API fails to load data.
- **Performance**: Loads in under 2 seconds and supports up to 100 concurrent users.
- **Recent Fixes**: 
  - Corrected table and chart labels from "Height (m)" to "Height (feet)" to match NOAA API units=english.
  - Bug #26 - X-axis labels showed "00:00" for monthly data (fixed in v1.3 with 2-day threshold).

## How to Run
The application is browser-based and runs in Google Chrome without additional software.

1. **Access via GitHub Pages**:
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
     ├── docs
     │   └── git-guide.md
     ├── image
     │   ├── background.jpg
     │   └── tide1.gif
     ├── index.html
     ├── README.md
     └── TestResults
         ├── KnownIssues.txt
         ├── ManualTests.txt
         ├── TestSummary.txt
         ├── UnitTestResults_jest.txt
         └── UserTests.txt
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

## Testing

### Unit Automatic Testing with Jest
The Tide Chart application employs Jest for unit testing to ensure the reliability of individual components in script.js. The unit tests, focus on key functions: parseTideData, updateTideTable, displayError, and validateDates. 
Please refer to TestResults/UnitTestResults_jest.txt

### Manual Test
Manual test reault please refer to TestResults/ManualTests.txt

### User Test
User test reault please refer to TestResults/UserTests.txt

## Known Issues
- **P2: No offline fallback**: Application does not display cached data during API downtime. - Reason: limited time and complexity of implementing offline storage.
- **P2: Date picker validation styling**: Invalid date range (end date before start) shows alert but lacks visual feedback. 
- **P2: Tide date range**: Data gathered from more than 10 years ago or predicted for more than 10 years in the future will not display. (This counts as an invalid date range, and the data is not gatherable from the API.)
- **P2: Overloading API**: NOAA API is overloaded when graph is created simultaneously with 20+ devices. Slows down graph creation significantly.
- **P2: Selectable tide data range**: Users are able to select non-viable dates from the drop down menu. i.e. dates like 1563.
please refer to TestResults/KnowIssues.txt

## Version Control
- **Branch**: `v1.3.0`
- **Tag**: `v1.3.0`.
