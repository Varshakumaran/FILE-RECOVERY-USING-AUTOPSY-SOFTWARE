# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:

<img width="1021" height="739" alt="image" src="https://github.com/user-attachments/assets/9e73884d-e5ea-4272-bee1-3b1bca37814f" />
<img width="1019" height="572" alt="image" src="https://github.com/user-attachments/assets/8c6eb8a5-654e-417c-8d24-97e05c6bddea" />
<img width="1033" height="601" alt="image" src="https://github.com/user-attachments/assets/08fafd6a-dc51-462b-b9fb-f7d32e8795f2" />
<img width="1029" height="607" alt="image" src="https://github.com/user-attachments/assets/e3d6fa15-36e5-4ab5-b09c-eb7cef90c3b7" />
<img width="1026" height="607" alt="image" src="https://github.com/user-attachments/assets/832a8583-1d3d-44c5-9281-6ec1a771dbcf" />
<img width="1024" height="609" alt="image" src="https://github.com/user-attachments/assets/cb5e5537-ec0c-4a89-a389-b6f2214187ea" />
<img width="1029" height="544" alt="image" src="https://github.com/user-attachments/assets/10f07f18-5046-42d1-a3bc-327c64a1506e" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
