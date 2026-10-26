# video-game-sales-excel-dashboard
Interactive Excel dashboard analyzing 16,598 video games and 8.9B units sold, using PivotTables, PivotCharts, and slicers. Key finding: Nintendo earned 20% of all sales from just 703 titles, selling about 3x more per game than Electronic Arts.

# Video Game Sales Dashboard (Excel)

## Overview
An interactive Excel dashboard analyzing 16,598 video games and 8.9 billion units sold 
worldwide. It uses PivotTables, PivotCharts, and slicers to show which genres, platforms, 
and publishers drive sales, how sales split by region, and how sales changed over time.

## Business Questions
1. Which genres sell the most, and which sell the most per game?
2. Which platforms dominate?
3. Which publishers lead the market?
4. How do sales split across regions?
5. How have sales changed over time?

## Dataset
Public video game sales dataset (`vgsales.csv`), 16,598 rows and 11 columns: name, 
platform, release year, genre, publisher, and sales in millions of units for North 
America, Europe, Japan, other regions, and globally.
Source: [add link to the original dataset page]

## Data Cleaning
- Checked for duplicate rows: none found.
- **271 games (1.6%) have no release year** and **58 (0.3%) have no publisher.** I left 
  these blank rather than guessing. Games without a year are excluded from the 
  year trend.
- Two titles (Madden NFL 13 and Wii de Asobu: Metroid Prime) each appear twice with 
  the same name, platform, year, and publisher but different sales figures. I kept both, 
  since they are likely separate releases rather than true duplicates, and flagged them.
- Kept the original data on a separate "Raw Data" sheet, untouched.
- Built PivotTables from the bounded Table range rather than full columns, so no 
  phantom "(blank)" categories appear.

## Dashboard Contents
| View | Question answered |
|---|---|
| Sales by Genre | Which genres sell the most |
| Sales by Platform (Top 10) | Which platforms dominate |
| Top 10 Publishers | Which publishers lead |
| Regional Sales | How sales split by region |
| Sales Trend by Year | How sales changed over time |

Slicers (Genre, Platform, Year) filter every view at once.

## Key Findings
- **8,920 million units sold** across 16,598 titles, an average of 0.54 million per title.
- **Action leads by total sales** (1,751M units, 19.6%), but mostly through volume: it 
  has the most titles of any genre (3,316) and averages only 0.53M per title.
- **Platform and Shooter games sell the most per title.** Platform averages 0.94M and 
  Shooter 0.79M. Adventure (0.19M) and Strategy (0.26M) have the lowest per-title 
  averages and the smallest shares (2.7% and 2.0%).
- **Four genres (Action, Sports, Shooter, Role-Playing) make up about 57% of all sales.**
- **PS2 is the best-selling platform** (1,256M units), followed by Xbox 360 (980M), 
  PS3 (958M), Wii (927M), and DS (823M). The top 10 platforms account for 76.5% of sales.
- **Nintendo is the standout publisher.** It earned 1,787M units (20% of all sales) from 
  only 703 titles, about 2.5M per title. Electronic Arts, second, earned 1,110M from 
  1,351 titles, about 0.8M per title. Nintendo sells roughly 3x more per game.
- **The top 10 publishers account for about 70% of sales**, out of roughly 580 publishers.
- **North America is nearly half the market** (49.3%), then Europe (27.3%), Japan 
  (14.5%), and other regions (8.9%).
- **Sales peaked in 2008** (679M units from 1,428 titles) and fell by roughly 60% by 2015.

## Recommendations
- **Judge genres by sales per title, not just total sales.** Action's total is largely 
  volume. Platform and Shooter titles return more per release, and Adventure and 
  Strategy return the least.
- **Prioritize North America and Europe for launches and marketing.** Together they 
  make up about 77% of sales.
- **Study Nintendo's franchise-driven model.** Its per-title average is about 3x that of 
  EA, which suggests fewer, stronger releases can outperform high-volume output.
- **Build around platforms with large install bases.** Ten platforms account for 
  over three quarters of all sales.
- **Get newer and digital sales data before drawing conclusions about recent years** 
  (see Limitations).

## Limitations
- **Data after 2016 is very sparse.** 2016 has 344 titles, and 2017-2020 have only 4 
  between them. The sharp drop in sales in those years reflects incomplete data, not 
  necessarily a real market collapse.
- Sales are estimates, and the dataset likely under-represents digital sales, which 
  grew after 2010. That may partly explain the decline after 2008.
- Regional columns don't add up exactly to the global column because of rounding.
- Platform and publisher totals reflect titles that appear in this dataset only.

## Tools Used
Microsoft Excel: PivotTables, PivotCharts, Slicers, SUMIFS/COUNTIFS formulas

## Repository Contents
- `Video_Game_Sales_Dashboard.xlsx`: full workbook (raw data, cleaned data, PivotTables, dashboard)
- `screenshots/`: dashboard and individual chart images

## How to Use
Download the workbook and open it in Excel. Click the slicers on the Dashboard sheet 
to filter all charts at once.
