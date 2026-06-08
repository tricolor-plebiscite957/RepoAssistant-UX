# RepoAssistant-UX 🐍

### 📚 What is this project?
This repository hosts Python automation utilities and user experience (UX) enhancements designed to help public and academic libraries in developing nations streamline their digital archiving and remote access systems.

---

### 🛠️ Features & Usage Code Blocks

#### 1. DSpace Bulk Metadata Upload
Automates the conversion and ingestion of large spreadsheets (Excel/CSV) into DSpace-compatible metadata structures.

```python
import pandas as pd

def prep_dspace_metadata(csv_file):
    # Read messy local spreadsheet
    df = pd.read_csv(csv_file)
    
    # Map fields to standard Dublin Core (dc) format
    dspace_df = pd.DataFrame({
        'dc.title': df['Book Title'],
        'dc.contributor.author': df['Author Name'],
        'dc.date.issued': df['Year'],
        'dc.subject': df['Keywords']
    })
    
    dspace_df.to_csv('dspace_bundle.csv', index=False)
    print("Successfully generated DSpace ingestion bundle!")

# Run the upload prep
prep_dspace_metadata('local_library_catalog.csv')
```

#### 2. Automated File & Directory Cleaning
Cleans up file names, removes corrupt characters, and structures book/manuscript folders before they are uploaded to institutional repositories.

```python
import os
import re

def clean_library_filenames(directory_path):
    for filename in os.listdir(directory_path):
        # Remove special characters and replace spaces with clean underscores
        clean_name = re.sub(r'[^a-zA-Z0-9._-]', '_', filename).strip()
        
        old_file = os.path.join(directory_path, filename)
        new_file = os.path.join(directory_path, clean_name)
        
        os.rename(old_file, new_file)
    print("Folder directory perfectly sanitized for DSpace upload!")
```

#### 3. Optimized Search Filtering for MyLoFT
Python helpers to parse and format e-journal subscription metadata feeds, ensuring clean indexing inside the MyLoFT app dashboard.

```python
def filter_myloft_feed(ejournal_data):
    optimized_records = []
    for record in ejournal_data:
        # Standardize discovery keywords for low-bandwidth mobile search
        record['search_tags'] = [tag.lower().strip() for tag in record['tags']]
        optimized_records.append(record)
    return optimized_records
```

#### 4. Remote Access Portal Link Builder for RemoteXS
Automatically generates proxy-wrapped access URLs so students can smoothly log in to electronic databases from outside the physical library building.

```python
def generate_remotexs_url(target_db_url, proxy_domain="remotexs.xyz.edu"):
    # Wraps an academic database URL with your library's RemoteXS proxy gateway
    secure_remote_link = f"https://{proxy_domain}/proxy?url={target_db_url}"
    return secure_remote_link

print(generate_remotexs_url("https://jstor.org"))
```

---

### 🚀 Getting Started

1. Clone this repository to your library computer:
   ```bash
   git clone https://github.com
   ```
2. Install the necessary Python packages:
   ```bash
   pip install pandas
   ```

---

### 💖 Support This Project
Developing and testing automation workflows for platforms like DSpace, MyLoFT, and RemoteXS takes massive amounts of development time. Keeping these tools free ensures underfunded institutions don't have to hire expensive software consultants.

Please support this open-source journey by clicking the **Sponsor** button at the top right of this page!



