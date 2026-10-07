# Orca Converter Cleaner

A lightweight HTML-based cleaner for Orca portfolio raw data. It parses pasted text, removes interface noise, and normalizes numeric output for easier downstream processing.

## Purpose

This tool simplifies Orca raw portfolio data by keeping only relevant portfolio and pool entries, cleaning malformed numeric values, and removing unneeded UI blocks.

## Key behaviors

- Starts processing from the first `Portfolio` entry.
- Normalizes range values and splits lower/upper bounds with `—`.
- Converts `k` units in price lines into full numeric values.
- Removes known header/footer blocks, including deposit asset intro text and `Vault Positions`.
- Replaces `Total Liquidity Value` with `Total Value`.
- Strips leading `$` from token names like `$WIF`.
- Removes leading dash-like prefixes from numeric values such as `– 0.0184`.
- Adds a leading zero to fractional values like `.0013`.
- Replaces `∞` with `—`, updates the preceding `0` to `0.003`, and inserts a new `0.05` line after the dash.
- Removes `N/A` lines and lines beginning with `+` without introducing extra blank lines.
- (add a text line)

## Usage

Open `_TML orca converter V4.6 _2026.04.27.html` in a browser, paste raw data into the textarea, and click `Clean Data` to view the cleaned result.

## Notes

The cleaner is self-contained in a single HTML file with inline CSS and JavaScript for simple editing and testing.
