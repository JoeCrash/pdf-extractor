# **PDF scraper v0.1.0**
`A tool to scrape text from pdf's.`

## **Software Goals**

### **User Workflow:**

    - User opens application
    - User loads a pdf file from URL or local
    - PDF uploads and displays.
    - Editor tools become available (Ignore Area, Extract Value, Extract Table Row, Grid Lines)
    - User adds grid lines, boxes (non tabled values) and boxGroups (table row/values) to the UI overlay
    - User gives each box and boxGroup id's. boxGroups are indexed
    - User saves overlay graphics into a job file.
    - User runs job.
    - On completion, User uploads, exports or saves

### **App Logic:**

    - App loads job file as a template
    - App creates folder with filename to hold working images
    - App breaks pdf up into pages and then snippets containing the text
    - App saves all the images to be processed
    - App generates a list of all the snippets to run OCR on
    - App runs OCR on each snippet.
    - App stores data as JSON key/value pairs
    - App completes job and returns data to UI


### **UI:**
  
    - Express / React Theme
    - PDF uploader
    - PDF viewer
    - Canvas/WebGL overlay for editor
    - File Wizard

### **App:**

    - Standalone exe or installer for entire applcation
    - Portable TesseractOCR or some auto installer
    - Upload to MySQL server
    - Export to XLS, CSV, DBF?, JSON
    - Save to Google Drive, Local Drive

