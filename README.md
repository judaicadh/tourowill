# Touro Will Beneficiaries — Interactive Dashboard
 
An interactive dashboard documenting the 65 bequests in the 1854 will of **Judah Touro** (1775–1854), American merchant and philanthropist.

## About
Judah Touro (June 16, 1775 – January 18, 1854) was an American businessman and philanthropist. In his will, he bequeathed $500,000 to institutions around the country—more than half of which went to non-Jewish causes. (As a percentage of GDP, these gifts would approximate $2 billion today.) 

The dashboard includes:
- Summary statistics (total amount, beneficiary count, cities reached, recipient types)
- An interactive map showing the geography of his gifts, with markers sized by total gift value at each location
- Bar charts showing the distribution of bequests by city and by recipient type
- A searchable, sortable ledger of all 65 bequests

## Files
 
| File | Purpose |
|------|---------|
| `index.html` | The complete dashboard. Fully self-contained — data is embedded, libraries load from CDN. |
| `TouroWill.csv` | The cleaned source data, provided for transparency and reuse. |
| `README.md` | This file. |


The column order in the embedded data is:
 
```
[Name, BequestNumber, TypeOfRecipient, TypeOfGift, GiftAmount, City, State, Country, Latitude, Longitude]
```
 
`GiftAmount` is a number for money gifts and `null` for property gifts.

## Notes on the data
 
- Two bequests of real property without a stated dollar value are recorded as `null`.
- Two London-based bequests have an empty `State of Recipient` field, since the column is U.S.-specific; the `Country of Recipient` column captures their location.
- Bequest numbers with decimals (e.g., `54.1`, `54.2`, `54.3`) indicate sub-clauses of a single combined bequest in the original will.

## Credits & technology

- Credit: Laura Newman Eckstein, Arnold and Deanne Kaplan Curator of Judaica Digital Humanities at the University of Pennsylvania Libraries
- Map: [Leaflet](https://leafletjs.com) with [CARTO Positron](https://carto.com/basemaps/) tiles. Map data © OpenStreetMap contributors.
- Charts: [Chart.js](https://www.chartjs.org).
- Ancestry.com. Massachusetts, U.S., Wills and Probate Records, 1635-1991 [database on-line]. Lehi, UT, USA: Ancestry.com Operations, Inc., 2015. Original data: Massachusetts County, District and Probate Courts.
- Fonts: Playfair Display and Crimson Pro via Google Fonts.
