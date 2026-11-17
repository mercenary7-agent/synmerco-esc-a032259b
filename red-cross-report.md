# American National Red Cross, tax return trend: revenue, expenses, assets and liabilities by tax year

## Answers
1. The CSV holds one row per filings_with_data entry returned, with its values as returned: 13 rows (tax years 2011-2023), each with tax_prd_yr, totrevenue, totfuncexpns, totassetsend, totliabend and pdf_url exactly as returned by the source (see Excerpts 1-13 below; the CSV is attached as data file D2 red-cross-returns.csv).
2. The CSV file is attached with exactly the listed columns, in order: tax_prd_yr, totrevenue, totfuncexpns, totassetsend, totliabend, surplus, net assets, revenue change, pdf_url (attached as D2 red-cross-returns.csv).
3. Surplus = totrevenue - totfuncexpns; net assets = totassetsend - totliabend; revenue change = change vs the previous entry in tax_prd_yr order, in percent (first entry 2011: none). All figures 2 decimals, half away from zero, computed from the unrounded returned values. Highlights: best surplus year 2018 (surplus 465018036.00 USD); worst surplus year 2012 (surplus -174615664.00 USD); average revenue growth 0.27% (mean of the 12 stated yearly changes). The year table below agrees with the attached CSV.

## Organization (as returned)
- Name: American National Red Cross
- State: DC

## Year table (sorted by tax_prd_yr)
| tax_prd_yr | totrevenue | totfuncexpns | totassetsend | totliabend | surplus | net assets | revenue change (%) |
|---|---|---|---|---|---|---|---|
| 2011 | 3452960387 | 3422010386 | 4253578616 | 2061654331 | 30950001.00 | 2191924285.00 | none |
| 2012 | 3154538043 | 3329153707 | 3777960071 | 2182737621 | -174615664.00 | 1595222450.00 | -8.64 |
| 2013 | 3412238741 | 3356880480 | 3898835153 | 1908777901 | 55358261.00 | 1990057252.00 | 8.17 |
| 2014 | 2974133836 | 3047227207 | 3791643231 | 1830884753 | -73093371.00 | 1960758478.00 | -12.84 |
| 2015 | 2726672619 | 2886003368 | 3486142571 | 1892332242 | -159330749.00 | 1593810329.00 | -8.32 |
| 2016 | 2618203252 | 2679603949 | 3235806694 | 2250133837 | -61400697.00 | 985672857.00 | -3.98 |
| 2017 | 2676037116 | 2808630913 | 3142581145 | 1946658460 | -132593797.00 | 1195922685.00 | 2.21 |
| 2018 | 3608002096 | 3142984060 | 3240247122 | 1658095198 | 465018036.00 | 1582151924.00 | 34.83 |
| 2019 | 2813454935 | 2937181875 | 3049904049 | 1607739689 | -123726940.00 | 1442164360.00 | -22.02 |
| 2020 | 2839409246 | 2683608516 | 3266899381 | 1454684272 | 155800730.00 | 1812215109.00 | 0.92 |
| 2021 | 3090183560 | 2796025309 | 3668499985 | 1300112674 | 294158251.00 | 2368387311.00 | 8.83 |
| 2022 | 3182229338 | 3048182336 | 3872181875 | 1171891777 | 134047002.00 | 2700290098.00 | 2.98 |
| 2023 | 3217077611 | 2971106889 | 4028321133 | 1008326202 | 245970722.00 | 3019994931.00 | 1.10 |

## Highlights
- Best surplus year: 2018, surplus 465018036.00 USD
- Worst surplus year: 2012, surplus -174615664.00 USD
- Average revenue growth: 0.27% (mean of the 12 stated yearly revenue changes)

## PROOF

### Request 1
- Request: GET https://projects.propublica.org/nonprofits/api/v2/organizations/530196605.json
- Retrieved (UTC): 2026-11-17T22:52:40Z
- HTTP status: 200
- Date header (first response): Tue, 17 Nov 2026 22:52:41 GMT

### Excerpt 0 (organization, exact as returned)
```
"organization":{"id":530196605,"ein":530196605,"name":"American National Red Cross","careofname":null,"address":"431 18TH ST NW","city":"Washington","state":"DC"
```
### Excerpt 1 (tax year 2011, exact as returned)
```
"tax_prd":201106,"tax_prd_yr":2011,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=2012_03_EO%2F53-0196605_990_201106.pdf","updated":"2017-06-29T23:37:24.001Z","totrevenue":3452960387,"totfuncexpns":3422010386,"totassetsend":4253578616,"totliabend":2061654331
```
### Excerpt 2 (tax year 2012, exact as returned)
```
"tax_prd":201206,"tax_prd_yr":2012,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=2013_03_EO%2F53-0196605_990_201206.pdf","updated":"2017-06-29T23:50:41.899Z","totrevenue":3154538043,"totfuncexpns":3329153707,"totassetsend":3777960071,"totliabend":2182737621
```
### Excerpt 3 (tax year 2013, exact as returned)
```
"tax_prd":201306,"tax_prd_yr":2013,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=2014_03_EO%2F53-0196605_990_201306.pdf","updated":"2017-06-30T00:05:45.017Z","totrevenue":3412238741,"totfuncexpns":3356880480,"totassetsend":3898835153,"totliabend":1908777901
```
### Excerpt 4 (tax year 2014, exact as returned)
```
"tax_prd":201406,"tax_prd_yr":2014,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=2015_03_EO%2F53-0196605_990_201406.pdf","updated":"2017-06-30T00:19:22.372Z","totrevenue":2974133836,"totfuncexpns":3047227207,"totassetsend":3791643231,"totliabend":1830884753
```
### Excerpt 5 (tax year 2015, exact as returned)
```
"tax_prd":201506,"tax_prd_yr":2015,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=2016_07_EO%2F53-0196605_990_201506.pdf","updated":"2017-06-30T00:37:49.920Z","totrevenue":2726672619,"totfuncexpns":2886003368,"totassetsend":3486142571,"totliabend":1892332242
```
### Excerpt 6 (tax year 2016, exact as returned)
```
"tax_prd":201606,"tax_prd_yr":2016,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=IRS%2F530196605_201606_990_2017091514741563.pdf","updated":"2018-12-10T23:10:29.110Z","totrevenue":2618203252,"totfuncexpns":2679603949,"totassetsend":3235806694,"totliabend":2250133837
```
### Excerpt 7 (tax year 2017, exact as returned)
```
"tax_prd":201706,"tax_prd_yr":2017,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=01_2018_prefixes_52-54%2F530196605_201706_990_2018011115111678.pdf","updated":"2018-12-10T23:07:31.595Z","totrevenue":2676037116,"totfuncexpns":2808630913,"totassetsend":3142581145,"totliabend":1946658460
```
### Excerpt 8 (tax year 2018, exact as returned)
```
"tax_prd":201806,"tax_prd_yr":2018,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=02_2019_prefixes_52-54%2F530196605_201806_990_2019021416097064.pdf","updated":"2019-10-15T18:36:18.369Z","totrevenue":3608002096,"totfuncexpns":3142984060,"totassetsend":3240247122,"totliabend":1658095198
```
### Excerpt 9 (tax year 2019, exact as returned)
```
"tax_prd":201906,"tax_prd_yr":2019,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=02_2020_prefixes_52-56%2F530196605_201906_990_2020020717122251.pdf","updated":"2021-08-30T18:32:09.297Z","totrevenue":2813454935,"totfuncexpns":2937181875,"totassetsend":3049904049,"totliabend":1607739689
```
### Excerpt 10 (tax year 2020, exact as returned)
```
"tax_prd":202006,"tax_prd_yr":2020,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=04_2021_prefixes_52-54%2F530196605_202006_990_2021042117979664.pdf","updated":"2022-07-01T20:34:48.242Z","totrevenue":2839409246,"totfuncexpns":2683608516,"totassetsend":3266899381,"totliabend":1454684272
```
### Excerpt 11 (tax year 2021, exact as returned)
```
"tax_prd":202106,"tax_prd_yr":2021,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=IRS%2F530196605_202106_990_2022030219681333.pdf","updated":"2023-08-07T19:42:52.665Z","totrevenue":3090183560,"totfuncexpns":2796025309,"totassetsend":3668499985,"totliabend":1300112674
```
### Excerpt 12 (tax year 2022, exact as returned)
```
"tax_prd":202206,"tax_prd_yr":2022,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=IRS%2F530196605_202206_990_2023060221351871.pdf","updated":"2024-08-28T20:14:04.511Z","totrevenue":3182229338,"totfuncexpns":3048182336,"totassetsend":3872181875,"totliabend":1171891777
```
### Excerpt 13 (tax year 2023, exact as returned)
```
"tax_prd":202306,"tax_prd_yr":2023,"formtype":0,"pdf_url":"https://projects.propublica.org/nonprofits/download-filing?path=download990pdf_03_2024_prefixes_41-54%2F530196605_202306_990_2024031222316430.pdf","updated":"2025-08-05T16:09:45.876Z","totrevenue":3217077611,"totfuncexpns":2971106889,"totassetsend":4028321133,"totliabend":1008326202
```

## synmerco-data

```synmerco-data
df795028b0657aca31e39beb61cc3b922d6ae4b3440805b33049f3cf533e9eab red-cross-returns.csv
```
