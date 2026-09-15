# Repeat PDF header on continuation pages

## What will change
- Make the complete PDF top section repeat on every generated page: company letterhead, document title, document number/date/page details, delivery address, account code, and order-by details.
- Keep the same document number on every page and replace the hard-coded page label with live “current page of total pages” numbering.
- Reserve matching space at the top of continuation pages so item rows never overlap the repeated header.
- Keep the existing item table, pallet configuration, and footer styling unchanged except where spacing is required for pagination.

## Verification
- Generate a long sample order that spans at least two pages.
- Render the PDF to images and visually inspect both pages for matching headers, correct document number/page count, and no overlapping or clipped content.

## Technical details
- Use React PDF’s fixed repeating content and dynamic page-number rendering in the existing PDF document component.
- Scope the update to generated/downloaded PDFs; the on-screen order preview remains unchanged.
