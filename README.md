# 🤖 abdelrhman-ellithy-rpa-multiple-web-scraping

This is a complete **UiPath RPA Project** that automates the process of reading product names from an Excel file, performing web searches, scraping results across multiple pages, and extracting key information like product title, price, and URL using advanced techniques such as RegEx. The results are then written to an output Excel file.

---

## 📌 Project Summary

✨ **Features:**

- 📥 Reads product search terms from an Excel sheet
- 🌐 Opens browser and performs product searches
- 📊 Scrapes web data across **multiple pages**
- 🔍 Extracts **Old Price** and **New Price** using **Regular Expressions**
- 📤 Writes the cleaned and structured data back to Excel
- 🗂️ Applies **dynamic file naming** using current DateTime

---

## 🧠 Main Automation Workflow

1. **Read Product List from Excel**
   - File: `Input/ProductsToBeScraped.xlsx`
   - Activities: `Excel Process Scope`, `Read Range`

2. **Search Each Product Online**
   - Uses `Use Application/Browser` with dynamic selectors
   - Types each product from the list into the search bar

3. **Scrape Multiple Result Pages**
   - Uses **Table Extraction Wizard** for:
     - 📌 Product Title
     - 💰 Price
     - 🔗 Product URL
   - Handles pagination using a **Next** button selector

4. **Extract Old and New Prices with RegEx**
   - Example expressions:
     ```vb
     System.Text.RegularExpressions.Regex.Match(input, "Old: \$([0-9.]+)").Groups(1).Value
     System.Text.RegularExpressions.Regex.Match(input, "New: \$([0-9.]+)").Groups(1).Value
     ```

5. **Write Scraped Data to Excel**
   - Writes to dynamically named file:  
     `ScrapedData_yyyyMMdd_HHmm.xlsx`

---

## 🛠️ Technologies & Components

- ✅ **UiPath Studio**
- 📄 Excel Activities (Read/Write)
- 🌍 Web Data Extraction
- 🧾 Regular Expressions
- 📁 File System Operations

---

## 📁 Project Structure
Directory structure:

Directory structure:
    ├── LICENSE
    ├── Main.xaml
    ├── project.json
    ├── Input/
    │   └── ProductsToBeScraped.xlsx
    ├── .local/
    │   ├── AllDependencies.json
    │   ├── dataManagerElementsOrder.json
    │   ├── nuget.cache
    │   ├── PackageCache.json
    │   ├── POC-Test.nuget.props
    │   ├── POC-Web Scrapping.nuget.props
    │   ├── ProjectSettings.json
    │   ├── db/
    │   │   └── references.db
    │   ├── HotReload/
    │   │   └── b1f0579f-80ae-4087-9643-1edd0315ee78
    │   ├── install/
    │   │   ├── POC-Test.Mapper.json
    │   │   └── POC-Web Scrapping.Mapper.json
    │   └── .globalvariables/
    ├── .objects/
    │   ├── .metadata
    │   ├── .type
    │   ├── H9Eb/
    │   ├── O0cj/
    │   └── pxq4/
    │       ├── .metadata
    │       ├── .type
    │       ├── jXd2/
    │       │   ├── .metadata
    │       │   ├── .type
    │       │   └── WHXt/
    │       │       ├── .metadata
    │       │       ├── .type
    │       │       ├── 6Dj-/
    │       │       │   ├── .metadata
    │       │       │   ├── .type
    │       │       │   └── .data/
    │       │       │       └── ObjectRepositoryTargetData/
    │       │       │           ├── .content
    │       │       │           ├── .hash
    │       │       │           ├── .attributes/
    │       │       │           │   └── SearchHash
    │       │       │           └── .images/
    │       │       │               └── .design/
    │       │       │                   └── 0rjFTcyPgnkGGAdt5LcAn5Q
    │       │       └── .data/
    │       │           └── ObjectRepositoryScreenData/
    │       │               ├── .content
    │       │               ├── .hash
    │       │               ├── .attributes/
    │       │               │   └── SearchHash
    │       │               └── .images/
    │       │                   └── .design/
    │       │                       └── 0NuvaegcizU22afsJEE3p6Q
    │       └── .data/
    │           └── ObjectSelectionName/
    │               ├── .content
    │               └── .hash
    ├── .screenshots/
    ├── .storage/
    │   └── .runtime/
    │       ├── AncestryPersistenceService/
    │       │   ├── 3e8b1179-bc31-464c-8e82-e4dd044ac061
    │       │   ├── 83c8c696-8515-4b5b-9ce6-4e9ea1fede98
    │       │   └── e340ade7-c1a4-4d5d-8f14-d5618907dbab
    │       └── DesignTimeTargetImagePersistenceService/
    └── .tmh/
        └── config.json


# RPA-Multiple-Web-Scraping
UiPath RPA Project – Web Scraping with Excel Integration
