# ShareVolume

## Summary
Your assigned company: Citizens Financial Group (CFG), CIK 0000759944.

Fetch https://data.sec.gov/api/xbrl/companyconcept/CIK0000759944/dei/EntityCommonStockSharesOutstanding.json (set a descriptive User-Agent per SEC guidance).
Read `.entityName`. Filter `.units.shares[]` for entries whose `fy` > "2020" and
includes a numeric `val`.
Save `data.json` with this structure:
`{"entityName": "Citizens Financial Group", "max": {"val": ..., "fy": ...}, "min": {"val": ..., "fy": ...}}`
where `max` and `min` refer to the highest and lowest `.val`. Break ties however you like.

Render a visually appealing `index.html` where:
- `<title>` and `<h1>` must include the live `entityName`.
- The max/min figures are clearly marked with these IDs:
  `share-entity-name`,
  `share-max-value`, `share-max-fy`,
  `share-min-value`, `share-min-fy`.

If the page is opened as `index.html?CIK=0001018724` (or any other 10-digit CIK),
`fetch()` from the SEC endpoint for that CIK using any proxy, e.g. AIPipe,
replace every ID listed above and the title and H1 without reloading the page.

Also commit the attachment uid.txt as-is.

## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/arnajit/ShareVolume.git
   cd ShareVolume
   ```

2. Open `index.html` in your browser or visit the GitHub Pages URL.

## Usage
Visit the live application at: https://arnajit.github.io/ShareVolume/

## Code Explanation
This project is a single-page web application built with HTML, CSS, and JavaScript. It follows the requirements specified in the brief and implements all requested functionality.

The application uses:
- Modern HTML5 structure
- Responsive CSS styling
- Vanilla JavaScript for interactivity
- External libraries loaded via CDN when needed

## Development History

### Round 1 - Initial Implementation (2025-10-22 14:08)
**Brief:** Your assigned company: Citizens Financial Group (CFG), CIK 0000759944.

Fetch https://data.sec.gov/api/xbrl/companyconcept/CIK0000759944/dei/EntityCommonStockSharesOutstanding.json (set a descriptive User-Agent per SEC guidance).
Read `.entityName`. Filter `.units.shares[]` for entries whose `fy` > "2020" and
includes a numeric `val`.
Save `data.json` with this structure:
`{"entityName": "Citizens Financial Group", "max": {"val": ..., "fy": ...}, "min": {"val": ..., "fy": ...}}`
where `max` and `min` refer to the highest and lowest `.val`. Break ties however you like.

Render a visually appealing `index.html` where:
- `<title>` and `<h1>` must include the live `entityName`.
- The max/min figures are clearly marked with these IDs:
  `share-entity-name`,
  `share-max-value`, `share-max-fy`,
  `share-min-value`, `share-min-fy`.

If the page is opened as `index.html?CIK=0001018724` (or any other 10-digit CIK),
`fetch()` from the SEC endpoint for that CIK using any proxy, e.g. AIPipe,
replace every ID listed above and the title and H1 without reloading the page.

Also commit the attachment uid.txt as-is.

**Features Implemented:**
- Initial application setup
- Core functionality as per requirements
- GitHub Pages deployment
- Responsive design

## License
This project is licensed under the MIT License - see the LICENSE file for details.
