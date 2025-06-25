# Drawing Register Application - User Guide & Overview

## What is the Drawing Register Application?

The Drawing Register Application is a **Windows desktop application** designed for engineering and construction companies to **manage, track, and distribute technical drawings and documents** throughout a project lifecycle. It provides a centralized system for document revision control, distribution management, and project reporting.

## Core Purpose & Benefits

### Primary Functions:
- **Document Management**: Organize and track engineering drawings, specifications, and technical documents
- **Revision Control**: Maintain complete history of document revisions with dates, purposes, and responsible parties
- **Distribution Tracking**: Monitor which documents have been distributed to which stakeholders and when
- **Project Organization**: Group documents by project with metadata like project numbers, disciplines, and client information
- **Reporting**: Generate professional PDF reports and transmittals for document distribution

### Key Benefits:
- **Centralized Control**: All project documents in one location with consistent metadata
- **Audit Trail**: Complete history of who received what documents and when
- **Professional Reporting**: Generate client-ready transmittals and distribution lists
- **Time Savings**: Batch operations and automated document scanning reduce manual work
- **Compliance**: Maintain proper document control standards required in engineering projects

## Main Application Features

### 1. Project Setup & Management
- Set project metadata (Project Number, Name, Discipline, Register Number, Client Number)
- Import documents from folder structures automatically
- Save and load project data for continued work

### 2. Document Grid & Viewing
- **Main Document Grid**: Central table showing all documents with key information
- **Dynamic Columns**: Automatically generates columns for each issue date
- **Filtering & Search**: Multiple search options (document number, description, type, etc.)
- **Date-based Filtering**: View documents issued on specific dates
- **Revision Display**: Color-coded revision information with visual indicators

### 3. Document Management
- **Add/Edit Documents**: Individual document metadata editing
- **Batch Operations**: Edit multiple documents simultaneously
- **Revision History**: Track all revisions with dates, purposes, methods, and responsible parties
- **File Linking**: Connect documents to their physical files for easy opening### 4. Distribution Management
- **Company Management**: Maintain list of distribution companies/stakeholders
- **Distribution Tracking**: Mark which documents were sent to which companies on which dates
- **Distribution Summary**: Visual overview of distribution status per issue date
- **Stakeholder Categories**: Organize recipients by type (Client, Contractor, Consultant, etc.)

### 5. Reporting & Output
- **PDF Reports**: Generate professional project document registers
- **Transmittals**: Create distribution transmittals showing what was sent to whom
- **Custom Filtering**: Reports can be filtered by date, folder, or other criteria
- **Professional Formatting**: Company branding and proper engineering document formatting

## User Interface Overview

### Main Window Layout:
1. **Top Section**: Project metadata input fields (Project No, Name, Discipline, etc.)
2. **Filter/Search Section**: Various filtering options and search tools
3. **Main Document Grid**: Central table displaying all documents and revisions
4. **Action Buttons**: Import, Edit, Batch Edit, Reports, Distribution management
5. **Status Information**: Distribution summaries and project statistics

### Key Dialog Windows:
- **Document Edit Dialog**: Edit individual document properties
- **Revision Edit Dialog**: Add/modify document revisions
- **Batch Edit Dialog**: Modify multiple documents at once
- **Distribution Dialog**: Manage stakeholder companies
- **Distribution Info Dialog**: View/modify distribution status

## Typical Workflow

### 1. Project Setup
1. Launch application
2. Enter project metadata (Project Number, Name, Discipline, etc.)
3. Import documents from project folder structure
4. Set up distribution companies/stakeholders

### 2. Document Management
1. Review imported documents in the main grid
2. Edit document metadata as needed (descriptions, types, packages)
3. Add revision information when documents are updated
4. Use batch edit for common changes across multiple documents### 3. Distribution Process
1. Filter documents by issue date
2. Mark which documents are distributed to which companies
3. Generate transmittal reports for distribution
4. Track receipt and acknowledgment

### 4. Ongoing Management
1. Regular imports to capture new/updated documents
2. Maintain revision history as documents evolve
3. Generate progress reports and document registers
4. Archive completed distributions

## File Organization

The application expects documents to be organized in a structured folder hierarchy, typically:
```
Project Folder/
├── project_data.json (application data)
├── distribution_list.json (company/stakeholder list)
├── Subfolder 1 (e.g., 20240315-IssueForConstruction)/
│   ├── Drawing1.pdf
│   ├── Drawing2.pdf
└── Subfolder 2 (e.g., 20240401-IssueForTender)/
    ├── Drawing1-Rev1.pdf
    └── NewDrawing.pdf
```

## Data Management

### Automatic Features:
- **Document Scanning**: Automatically discovers PDF files in folder structure
- **Metadata Extraction**: Parses document numbers, types, and descriptions from filenames
- **Revision Detection**: Identifies document revisions and purposes from folder names
- **Date Recognition**: Extracts issue dates from folder naming conventions

### Manual Input Required:
- Project metadata (numbers, names, disciplines)
- Distribution company setup
- Distribution tracking (marking which documents go to which companies)
- Custom document descriptions or corrections to auto-detected information## Best Practices for Usage

### 1. Folder Organization
- Use consistent date-based folder naming (YYYYMMDD format)
- Include purpose in folder names (e.g., "20240315-Construction", "20240401-Tender")
- Maintain consistent file naming conventions

### 2. Document Management
- Regularly import new documents to keep register current
- Use batch edit for efficient metadata updates
- Maintain accurate revision information
- Keep distribution tracking up to date

### 3. Project Setup
- Complete all project metadata before starting document management
- Set up all distribution companies before first distribution
- Save project data regularly (automatic on many operations)

## Technical Requirements

- **Operating System**: Windows 10/11
- **Framework**: .NET 8.0
- **File Types Supported**: Primarily PDF documents
- **Storage**: Local file system (no database server required)
- **Network**: Not required (fully standalone application)

## Support Information

### Common File Locations:
- **Project Data**: Stored in `project_data.json` in the project folder
- **Distribution Lists**: Stored in `distribution_list.json` in the project folder
- **Application Logs**: `output.log` in application directory

### Getting Help:
- Check folder structure matches expected format
- Verify PDF files are not corrupted or password-protected
- Ensure project metadata is complete before generating reports
- Use "Refresh View" button if display appears outdated

This application is designed to streamline document management workflows in engineering projects while maintaining professional standards for document control and distribution tracking.