# HTML Tide Chart

## MVP
Display tide predictions for Seattle, WA (Puget Sound, NOAA station 9447130). The Minimum Viable Product (MVP) fetches tide data from NOAA’s CO-OPS API and presents it in a table (high/low tides) and a graph (hourly tide heights) for the current date.

### Fixed Scope
- Currently supports only Seattle tides for today’s date (custom date input deferred to prototype due to API issues).

## How To Run
1. Clone repository:
```
git clone https://github.com/zjttyl/project3-TideChart.git
cd project3-TideChart
```

2. Start a local server
```
python -m http.server
```

3. Open a browser and navigate to http://localhost:8000.

## Resources
- [Git Guide for Team GYYKS](docs/git-guide.md)

## Version Control
- Use branches for versions (e.g., `prototype`, `v1.1`) instead of duplicate files.
- Main branch is protected; use freature branches and PRs for changes.
- See [Git Guide](docs/git-guide.md) for instructions.

