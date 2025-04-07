
# 📊 Netflix Dataset Cleaner

This project contains a Python script to **clean and preprocess a raw Netflix dataset** (`netflix_titles.csv`) using **Pandas**. It's designed to run smoothly in **Google Colab** or any Python environment.

---

## 📌 Objective

Clean a raw dataset by:
- Handling missing values
- Removing duplicates
- Standardizing text formats
- Converting date formats
- Cleaning column headers
- Fixing data types

---

## 🧰 Tools Used

- Python 3
- Pandas
- Google Colab (or Jupyter Notebook)

---

## 🚀 How to Run

1. Upload the raw `netflix_titles.csv` file to your Colab session.
2. Run the cleaning script (`netflix_cleaning_script.ipynb` or the provided Python code).
3. A cleaned dataset named `cleaned_netflix_titles.csv` will be generated and saved.

---

## 🧹 Cleaning Steps

The script performs the following:

1. **Load Data**  
   Reads `netflix_titles.csv` using Pandas.

2. **Missing Values**  
   - Displays count of nulls using `.isnull()`
   - Drops rows missing essential fields like `title`
   - Fills missing values in `country`, `cast`, `director`, and `rating` with defaults

3. **Duplicates**  
   Removes duplicate rows using `.drop_duplicates()`

4. **Text Standardization**  
   - Standardizes `type`, `country`, and `rating` columns using `.str.strip()`, `.str.lower()`, `.str.title()`

5. **Date Conversion**  
   Converts `date_added` column to `datetime` format using `pd.to_datetime()`

6. **Column Cleaning**  
   Cleans column names to lowercase, no spaces, using `.str.lower().str.replace(" ", "_")`

7. **Data Type Fixes**  
   - Converts `release_year` to integer
   - Ensures `date_added` is `datetime`

8. **Save Cleaned Data**  
   Outputs a cleaned CSV file: `cleaned_netflix_titles.csv`

---

## ✅ Output

- Cleaned dataset: `cleaned_netflix_titles.csv`
- Summary printed to the console (shape, missing values, data types)

---

## 📎 Example Dataset Columns

- show_id
- type
- title
- director
- cast
- country
- date_added
- release_year
- rating
- duration
- listed_in
- description

---

## 📬 Contact

If you have suggestions or want to expand this cleaning pipeline, feel free to open an issue or fork the repo!
