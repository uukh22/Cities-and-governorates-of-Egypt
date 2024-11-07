# Egypt Regions Data Insert Script

This SQL script populates tables `Governments` and `Cities` with data representing various governments (or governorates) in Egypt and their respective cities. The data includes both Arabic and English names for easy reference and localization.

## Tables Overview

1. **Governments Table**: Contains the names of Egypt's governorates in both Arabic and English.
   - **Columns**:
     - `Government_Name_AR`: Arabic name of the governorate.
     - `Government_Name_EN`: English name of the governorate.

2. **Cities Table**: Lists cities within each governorate, with the city names in both Arabic and English.
   - **Columns**:
     - `GovernmentId`: References the ID of the governorate (assumes a `GovernmentId` foreign key).
     - `City_Name_AR`: Arabic name of the city.
     - `City_Name_EN`: English name of the city.

## Instructions

1. **Run the script** in an SQL-compatible environment (e.g., MySQL, PostgreSQL, or other relational database systems).
2. **Ensure that tables `Governments` and `Cities` exist** with the proper schema and relationships:
   - `Governments` table should have an auto-increment primary key.
   - `Cities` table should reference the `Governments` table's primary key (`GovernmentId`).
   
3. **Execute** each `INSERT INTO` statement sequentially or as a single transaction.

## Data Description

- **Governorates (Governments Table)**: Each governorate is listed with its Arabic and English name, such as `Cairo (القاهرة)`, `Giza (الجيزة)`, etc.
- **Cities (Cities Table)**: Cities are grouped by governorate, with the `GovernmentId` corresponding to the appropriate governorate ID.

## Example Data

### Governments Table

| Government_Name_AR | Government_Name_EN |
|--------------------|--------------------|
| القاهرة            | Cairo              |
| الجيزة             | Giza               |
| الأسكندرية         | Alexandria         |

### Cities Table

| GovernmentId | City_Name_AR   | City_Name_EN     |
|--------------|----------------|------------------|
| 1            | 15 مايو         | 15 May           |
| 1            | الأزهر         | Al Azhar         |
| 2            | الجيزة         | Giza             |
| 2            | الدقي         | Dokki            |

## Notes

- The data is provided in UTF-8 encoding to support Arabic characters.
- Make sure that any database collation and character set configurations support Arabic text, such as `utf8mb4` for MySQL.

## License

This script is open for use and modification. Ensure data accuracy when applying changes.
