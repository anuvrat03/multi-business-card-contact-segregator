# Contact Text → Segregated .vcf (vCard) & Share Tool

A lightweight, single-file browser utility built for **GitHub Pages** that parses structured or bulleted contact blocks into segregated fields, generates standard **vCard 3.0 (`.vcf`)** output, and shares or downloads the file on mobile and desktop browsers.

## Features

- **Field Segregation:** Extracts `Name`, `Title`, `Company`, `Phone`, `Email`, and `Address` from raw text blocks (including leading bullet/separator characters such as `·`, `•`, `-`, or `*`).
- **Multi-Phone Splitting:** Splits multiple phone numbers separated by `/` or `|` into individual vCard `TEL` entries (`CELL` for the first number, `WORK` for subsequent numbers).
- **Multi-Contact Batching:** Automatically splits multiple pasted contacts starting at each `Name:` entry, lets you cycle through them with **Prev** and **Next**, and exports all of them into a single `.vcf` file.
- **Browser Templates (`localStorage`):** Save, reload, and delete reusable input templates locally in the browser without a backend server.
- **Share & Download:** Uses the Web Share API (`navigator.share` with `files`) where supported to open the native share sheet (such as **Contacts** on Android), with a direct `.vcf` file download fallback.

## Supported Input Format

Paste one or more contacts structured with labeled fields:

```text
Name: VENKAT KAMBALA
· Title: AREA SALES MANAGER
· Company: LABINDIA ANALYTICAL
· Phone: +91 9676957084 / 040-4444 3530
· Email: venkat.kambala@labindia.com
· Address: # 1-3-37, CP Chamber, 2nd Floor, Street No: 5, Habsiguda, Hyderabad - 500 007.
