# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains documentation for the **Drawing Register Application**, a Windows desktop application designed for structural engineering firms and construction companies to manage, track, and distribute structural drawings and technical documents throughout project lifecycles.

### Core Architecture
- **Application Type**: Windows desktop application (.NET 8.0)
- **Purpose**: Document management, revision control, and distribution tracking for engineering projects
- **Primary Users**: Structural engineers, project managers, document controllers
- **File Types**: Primarily PDF technical drawings and specifications

## Key System Components

### Document Management System
- Automated scanning of folder structures containing PDF files
- Revision tracking with complete audit trails
- Professional PDF report generation and transmittals
- Integration with Bluebeam Revu for PDF viewing

### Data Storage
- `project_data.json`: Document metadata and revision history
- `distribution_list.json`: Company and stakeholder information  
- Local file system storage (no database server required)
- Folder-based organization with date-coded issue directories

### Distribution Workflow
The application follows a three-step process:
1. **File Preparation**: Create dated folders (YYYYMMDD-PURPOSE-DESCRIPTION or YYYYMMDD_PURPOSE ISSUE_RevCode) with PDFs
2. **Register Update**: Scan folders, batch edit properties, assign distributions
3. **Transmittal Generation**: Filter by issue date and generate professional PDF reports

## Expected Folder Structure

```
\\srmjfp01\data\02-PROJECTS\17700 - FILES\17749\02 - ENG\02 - DRAWINGS\03 - OUTGOING\01 - PDF
├── project_data.json (created by app)
├── distribution_list.json (created by app)  
├── 20250203-TENDER-ISSUE/
│   ├── 17749-M+J-S1-XX-DR-S-00-01-T01-GENERAL-NOTESHEET 1.pdf
│   └── 17749-M+J-V1-F1-DR-S-16-01-T01-WAREHOUSE-FOUNDATION-PLAN.pdf
└── 20250411_CONSTRUCTION ISSUE_C01/
    ├── 17749-M+J-V1-F1-DR-S-16-01-C01-WAREHOUSE-FOUNDATION PLAN.pdf
    └── Transmittal_17749-M+J-00-XX-RE-Z-00-01_20250415.pdf
```

## Documentation Structure

### Current Documentation Files
- `docs/Application-Overview.md`: High-level application description and core functionality
- `docs/Complete-User-Guide.md`: Comprehensive tutorial and user instructions with step-by-step workflows
- `docs/gemini.md`: Empty file (purpose unclear)

### Documentation Standards
- Professional engineering document formatting
- Step-by-step workflows with visual diagrams
- Troubleshooting sections with common issues and solutions
- Best practices for file organization and naming conventions

## Key Naming Conventions

### Folder Naming
- Format: `YYYYMMDD-PURPOSE-DESCRIPTION` or `YYYYMMDD_PURPOSE ISSUE_RevCode`
- Examples: `20250203-TENDER-ISSUE`, `20250411_CONSTRUCTION ISSUE_C01`, `20250415-CONSTRUCTION ISSUE`

### Document Naming (M+J Company Format)
- Format: `[ProjectNumber]-M+J-[Building]-[Level]-[DocumentType]-[Discipline]-[SheetNumber]-[RevisionCode]-[Description].pdf`
- Examples: `17749-M+J-V1-F1-DR-S-16-01-C01-WAREHOUSE-FOUNDATION PLAN.pdf`
- Revision Codes: C01 (Construction Issue 01), T01 (Tender Issue 01), P01 (Planning Issue 01), I01 (Information Issue 01)
- Project Numbers: 5-digit format (17749, 240478, 230049)
- Company Code: Always "M+J"

## Development Context

This is a **documentation-only repository** - no source code is present. The repository focuses on:
- User guides and tutorials with M+J company-specific examples
- Application overview and architecture
- Best practices and workflows for structural engineering projects
- Troubleshooting and FAQ content
- Real project examples from M+J Engineering projects (Glendroanch, Glenfiddich, Longmorn)

When working with this documentation:
- Maintain professional engineering documentation standards
- Use clear, step-by-step instructions
- Include visual aids (diagrams, tables) where helpful
- Focus on practical workflow guidance
- Keep content current with application features