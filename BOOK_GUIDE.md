# Tracop Book Club — Book Data Guide

This document defines the rules, categories and metadata used for books on the Tracop Book Club website.

The purpose of this guide is to keep book information consistent as the collection grows.

---

## 1. Language

All website content and book metadata must be in English.

The club reads books in English. Therefore, books must be listed using the title of the English-language edition that club members will read, even when the work was originally published in another language.

Example:

- Country: Spain
- Title: *Woodworm*
- Author: Layla Martínez
- Translators: Sophie Hughes and Annie McDermott

The title of the original-language edition does not need to be displayed on the website.

---

## 2. Country

Each book is associated with a country for the purpose of the world map.

Country names must always be written in English.

Each country has:

- Country name
- Country code
- Flag
- Latitude
- Longitude

All books associated with the same country share one map pin.

Selecting the country pin displays all books associated with that country.

---

## 3. Categories

Categories are controlled vocabulary used to keep filtering consistent.

A book may have more than one genre.

### Form

- Fiction
- Non-fiction
- Poetry
- Drama
- Graphic Novel
- Short Stories
- Essays
- Memoir

### Genre

- Horror
- Mystery
- Thriller
- Crime
- Fantasy
- Science Fiction
- Romance
- Historical Fiction
- Literary Fiction
- Adventure

Additional genres may be added when needed, but existing categories should be preferred whenever possible.

### Period

- Contemporary
- Classic

---

## 4. Club status

Each book has one current status.

### `recommendation`

The book is included on the map as a general recommendation but has not been formally proposed for a club vote.

### `proposed`

The book has been formally proposed as a potential club read.

### `read`

The book has already been read by the club.

Being the current monthly book is NOT a status.

Monthly selections are managed separately through the `monthlyFeature` field.

---

## 5. Monthly feature

The book currently being read by the club may be highlighted as the monthly feature.

Example:

    "monthlyFeature": {
      "active": true,
      "month": "December",
      "year": 2026
    }

Only the current monthly book should normally have `active` set to `true`.

Previous monthly selections may retain their month and year while having `active` set to `false`.

This information may later be used to create a history of previous club reads.

---

## 6. Ratings

The rating displayed depends on whether the club has already read the book.

### Books not yet read

Use the Goodreads rating when available.

The website will:

- identify the rating as "Goodreads"
- display the rating in grey
- link to the Goodreads page

Goodreads ratings may change over time.

### Books already read

Use the average rating given by Tracop Book Club members.

The website will:

- identify the rating as "Club rating"
- visually distinguish it from external ratings
- optionally display the number of club votes

The Goodreads link may still be provided for reviews and additional information.

---

## 7. Translators

For books originally published in another language, translators of the English edition should be recorded when known.

Example:

- Author: Layla Martínez
- Translated by Sophie Hughes and Annie McDermott

This field may be omitted for books originally written in English.

---

## 8. Availability

Whenever possible, include legitimate places where club members can access the English-language edition.

Priority should be given to:

- Public library catalogues
- Digital public library services
- University or institutional library catalogues
- Other legitimate borrowing services

Availability must refer specifically to the English-language edition whenever possible.

Each availability entry may include:

- Service or library name
- Type of service
- Format
- Direct URL to the catalogue record

Examples of formats:

- Physical book
- E-book
- Audiobook

The website should not imply that a book is currently available for loan unless this can be confirmed by the linked service.

---

## 9. Goodreads

When available, each book should include a direct link to its Goodreads page.

Goodreads is used for:

- External ratings for books not yet read by the club
- Reader reviews
- Additional information about the book

Goodreads ratings should not replace the club rating after a book has been read.

---

## 10. Cover images

Each book should display the cover of the English-language edition represented on the website.

Cover files are stored in:

    images/covers/

File names should use lowercase letters and hyphens.

Example:

    woodworm.jpg

---

## 11. Book proposals

Book proposals will eventually be submitted through the website.

Suggested information to collect:

- Name of proposer
- Country
- English title
- Author
- Translator(s), when applicable
- Genre
- Reason for recommending the book
- Goodreads URL
- Library or availability links, when known

Submitted books should be reviewed before being added to the website.

---

## 12. Website filters

The map and book collection may be filtered using:

### Country
Example: Spain, Japan, Argentina

### Form
Example: Fiction, Poetry, Memoir

### Genre
Example: Horror, Romance, Historical Fiction

### Period
- Contemporary
- Classic

### Club status
- Recommendation
- Proposed
- Read

These filters should use the controlled categories defined in this document.
