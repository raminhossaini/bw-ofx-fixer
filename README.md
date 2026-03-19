# bw-ofx-fixer

A single-page browser tool that fixes OFX files exported from Bank Windhoek (Namibia) so they can be imported into [Actual Budget](https://actualbudget.org/) or any other finance app.

## The problem

Bank Windhoek's OFX exports are not fully OFX-compliant:

- `<TRNTYPE>` uses `DR` / `CR` instead of the required `DEBIT` / `CREDIT`
- Debit `<TRNAMT>` values are positive instead of negative

## What it does

- Replaces `DR` → `DEBIT` and `CR` → `CREDIT`
- Negates the amount on all debit transactions

## Usage

Open `index.html` in a browser. Upload, drag-and-drop, or paste your OFX file. The fixed output appears instantly — copy it to the clipboard or download it as a file.

Everything runs client-side; no data leaves your browser.
