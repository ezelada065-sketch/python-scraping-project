
## Author
Edgar Zelada
Python Developer



# 📚 Books Web Scraper with SQLite Database

## 📌 Project Overview

This project is a complete web scraping pipeline developed in Python that extracts book data from:

👉 http://books.toscrape.com/

The scraper collects structured information for every book across all categories and stores the data in a normalized SQLite relational database.

---

## 🚀 Features

- Extracts all book URLs from every category
- Handles pagination automatically
- Scrapes detailed book information:
  - Title
  - Price
  - Rating (converted to numeric)
  - Availability
  - Category
  - Description
  - UPC (unique identifier)
- Normalized relational database design
- Many-to-many relationship between books and authors
- Retry logic for SQLite locking issues
- Analytical queries using Pandas

---

## 🛠 Technologies Used

- Python 3
- requests
- BeautifulSoup4
- SQLite3
- Pandas
- Jupyter Notebook

---

## 🗄 Database Schema

### Authors
| Field | Type |
|-------|------|
| id (PK) | INTEGER |
| name | TEXT (UNIQUE) |

### Books
| Field | Type |
|-------|------|
| id (PK) | INTEGER |
| title | TEXT |
| price | REAL |
| rating | INTEGER |
| availability | TEXT |
| category | TEXT |
| description | TEXT |
| upc | TEXT (UNIQUE) |

### Book_Author (Many-to-Many)
| Field | Type |
|-------|------|
| book_id (FK) | INTEGER |
| author_id (FK) | INTEGER |

---

## ⚙️ Installation



