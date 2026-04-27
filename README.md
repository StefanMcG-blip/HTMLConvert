# Orca Converter Cleaner

This repository contains a lightweight HTML-based data cleaner for Orca portfolio raw text.

## Purpose

The tool accepts pasted raw portfolio data and transforms it into a simplified cleaned output by removing UI clutter, normalizing numeric ranges, and filtering irrelevant lines.

## Key behaviors

- Keeps content starting from the first `Portfolio` entry.
- Normalizes range values and splits them into lower/upper values separated by `—`.
- Converts `k` units in price lines into full numeric values.
- Removes known header and footer blocks such as deposit asset intro text and `Vault Positions`.
- Replaces `Total Liquidity Value` with `Total Value`.
- Strips leading `$` from token names like `$WIF`.
- Removes leading dash-like prefixes from numeric lines such as `– 0.0184`.
- Replaces `∞` with `—`, updates the preceding `0` to `0.003`, and inserts a new `0.05` line after the dash.
- Removes `N/A` lines and lines starting with `+` without adding extra blank lines.

## Usage

Open `_TML orca converter V4.6 _2026.04.27.html` in a browser, paste raw data into the textarea, and click `Clean Data` to view the cleaned result.

## Notes

This file is intentionally self-contained with inline CSS and JavaScript for quick edits and testing.
