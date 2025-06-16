# RPA-Multiple-Web-Scraping

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
    ├── Output/
    │   └── ScrappedData2025-06-16-09-48.xlsx
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
    ├── .screenshots/
    ├── .storage/
    │   └── .runtime/
    │       └── DesignTimeTargetImagePersistenceService/
    └── .tmh/
        └── config.json


## 📄 License

This project is licensed under the terms of the **MIT License**. See the [LICENSE](./LICENSE) file for details.