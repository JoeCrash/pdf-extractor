# **PDF scraper v0.1.0**
`A tool to scrape text from pdf's.`

## **Software Goals**

### **Todo's**
**0.1.0**
- Install libraries
- Setup portable Tesseract
- Secure sensitive info
- Develop Structure
- Setup webserver

**v 0.2.0**
  - Prototype Frontend
  - Add File Uploader
  - Add PDF display
  - Prototype Drawing Tools using canvas or other
  - Develop Job File (stores key:coordinate pairs for the snippets to cut)

**v 0.3.0**
  - Convert draw objects into a job file
  - Add sharp to cut image snippets using job file
  - Add Tesseract to run OCR on image snippets

**v 0.4.0**
  - Develop persistence for extracted data
  - Add Remove Cache to UI, for cleanup of old jobs
  - Develop some software adjustments to scanned text based on errors encountered

**v 0.5.0**
  - Prototype exporting of scanned data
  - Bugfixes
  - Add Testing

**v 0.6.0 - v 1.0.0**
- Additional Feature Development
- Development Roadmap
- Developer Documentation
- User Documentation
- Usage Examples
- Pull Request Requirements
- Revisit License
- Release into the wild

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

### **UI Features:**
    - PDF uploader
    - PDF viewer
    - Canvas/WebGL overlay for editor
    - File Wizard

### **Libraries/Frameworks/Runtime:**
    - Node.js - Runtime
    - Express - Middleware
    - React - Frontend
    - Something for drawing tools/interface (Pixi.js, d3.js, etc) - Drawing Tools
    - Internal Storage (SQL lite?, json) - Data Persistence
    - Axios or FS - PDF Loader
    - Sharp - Image manipulation, snippet generation
    - TesseractOCR & Tesseract.js for node - Scan Text
    - nw.js - Standalone software, installers, etc

### **App Wants:**
    - 100% coverage testing
    - Standalone exe or installer for entire applcation
    - Portable TesseractOCR or some auto installer
    - Upload to MySQL server (schema generator?)
    - Export to XLS, CSV, DBF?, JSON
    - Save to Google Drive, Local Drive
    - Distribution to local network if app runs on distributed mode

