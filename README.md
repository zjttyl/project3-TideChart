# HTML Tide Chart

## Introduction
Display tide predictions for Seattle, WA (Puget Sound, NOAA station 9447130). The prototype fetches tide data from NOAA’s CO-OPS API and presents it in a table (high/low tides) and a graph (hourly tide heights) for the current date.

### Fixed Scope
- Currently supports only Seattle tides for today’s date

## Prototype Release
- **Version**: v0.1.1-prototype
- **Release**: [GitHub Release](https://github.com/zjttyl/project3-TideChart/releases/tag/v0.1.1-prototype)
- **Run Instructions**:
1. Clone: `git clone https://github.com/zjttyl/project3-TideChart.git`
2. Checkout prototype: `git checkout prototype`
3. Navigate: `cd project3-TideChart`
4. Start server: `python3 -m http.server`
5. Open: `http://localhost:8000`
- **UI and Functionality**:
  - Table: High/low tide predictions for Seattle (NOAA station 9447130, today's date)
  - Graph: Hourly tide heights.
- **How to use**:
  - Open browser: `http://localhost:8000`
  - Basic UI: Navigation and click "Get Tides for Today" to view tides.
- **P0 Requirements Met**:
  - Display daily tide predictions in a table.
  - Visualize tide data in a graph.

## Resources
- [Git Guide for Team GYYKS](docs/git-guide.md)

## Version Control
- Use branches for versions (e.g., `prototype`, `v1.1`) instead of duplicate files.
- See [Git Guide](docs/git-guide.md) for instructions.

