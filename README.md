# LeaseMaster HK｜掌租人

A lightweight, browser-based property tenancy management demo for Hong Kong landlords. Keep property and tenant records together, track rent and utility settlements, and prepare printable receipts.

**Live demo:** [bellahkust.github.io/-lease-master-hk](https://bellahkust.github.io/-lease-master-hk/)

## Features

- Manage property addresses, units, tenant details, tenancy dates, rent schedules, management fees, and rates.
- Track rent due and paid amounts, then mark each unit as settled.
- Calculate water and electricity charges for subdivided units from meter readings and the total bill amount and usage.
- Treat a property with no unit number as a whole-unit tenancy, without apportioning utilities.
- Print or save rent and utility receipts as PDF through the browser.
- Switch between Traditional Chinese, Simplified Chinese, and English.
- Use the responsive interface on desktop and mobile.

## Getting started

LeaseMaster HK is a standalone HTML app. It has no build step or package dependencies.

1. Download or clone this repository.
2. Open [index.html](index.html) in a modern web browser.
3. Select **進入管理平台 / Enter platform** on the welcome screen.

You can also serve the folder with any static file server or host it on GitHub Pages.

## Utility calculation

For subdivided properties, each unit's utility charge is calculated as:

```
Unit charge = (current meter reading - previous meter reading)
              × total bill amount ÷ total bill usage
```

A property with no unit number is treated as a whole-unit tenancy and charged the full bill amount.

## Data storage

Property and tenancy records are stored in the current browser's local storage. They are not uploaded to a server and do not sync between browsers or devices. Clearing browser site data may remove saved records. Use sample information when exploring the demo.

## Project structure

```
.
└── index.html   # Interface, styles, translations, and client-side app logic
```

## Scope

This project is a prototype for demonstrating a simple tenancy and settlement workflow. It does not include account login, cloud synchronization, online payments, or server-side data storage. Review generated receipts before using them.

---

## 繁體中文簡介

**掌租人 LeaseMaster HK** 是為香港業主設計的物業租務管理 Demo，可管理物業及租戶資料、記錄租金結算，並按水錶和電錶讀數分攤分間單位的水電費。平台支援繁體中文、簡體中文和英文，並可透過瀏覽器列印或另存 PDF 收據。

本專案為單一 HTML 檔案，不需安裝或建置。直接以瀏覽器開啟 [index.html](index.html) 即可試用。資料只儲存在目前瀏覽器的本機儲存空間，不會上傳或跨裝置同步。
