# PI Planning Dashboard - User Guide

**Version:** 1.0.0  
**Last Updated:** March 2026

---

## Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Dashboard Overview](#dashboard-overview)
4. [Know Your Team (KYT)](#know-your-team-kyt)
5. [Capacity Planning](#capacity-planning)
6. [Checklist](#checklist)
7. [Guidelines](#guidelines)
8. [Configuration](#configuration)
9. [Export & Reporting](#export--reporting)
10. [Data Management](#data-management)
11. [Best Practices](#best-practices)
12. [Troubleshooting](#troubleshooting)
13. [FAQ](#faq)

---

## Introduction

The **PI Planning Dashboard** is a comprehensive, browser-based application designed to streamline Program Increment (PI) planning activities. It provides an intuitive interface for team capacity planning, resource management, and quality tracking.

### Key Features

- ✅ **Self-contained** - Runs entirely in your browser, no server required
- ✅ **Auto-save** - Data persists automatically in browser storage
- ✅ **Export Ready** - Multiple export formats (PDF, CSV, JSON)
- ✅ **Responsive** - Works on desktop, laptop, and tablet devices
- ✅ **Offline Capable** - No internet connection needed after initial load
- ✅ **Zero Installation** - Just open the HTML file and start planning

### System Requirements

- **Browser:** Chrome 90+, Edge 90+, Firefox 88+, Safari 14+
- **Operating System:** Windows, macOS, or Linux
- **Storage:** ~2MB of browser local storage
- **No Internet Required** (after initial file access)

---

## Getting Started

### Quick Start (5 Minutes)

1. **Open the Dashboard**
   ```
   - Locate the file: index.html
   - Double-click to open in your default browser
   - OR right-click → Open with → [Your Browser]
   ```

2. **First Time Setup**
   - The dashboard opens with an empty template
   - Navigate to **Configuration** tab
   - Fill in required fields (marked with validation)
   - Click **Save Configuration**

3. **Add Your First Team Member**
   - Navigate to **KYT** tab
   - Fill in the form with team member details
   - Click **Add Member**
   - Member appears in the team members grid

4. **View Dashboard**
   - Click **Dashboard** in the sidebar
   - See your team overview, capacity summary, and statistics

### What You'll See on First Launch

- **Empty Dashboard** - Ready for you to build your PI plan
- **Navigation Sidebar** - Access to all major sections
- **Header** - Shows PI badge, status, and reset button
- **Toast Notification** - "Dashboard initialized with empty template"

---

## Dashboard Overview

The **Dashboard** is your command center, providing a bird's-eye view of your PI plan.

### Components

#### 1. **Page Header**
- **PI Name Badge** - Current PI identifier
- **Status Indicator** - Real-time status (Draft/In-Review/Approved/Active)
- **Clock** - Current time display
- **Reset Button** - Start fresh with empty template

#### 2. **Statistics Cards**
- **Team Size** - Total active members
- **Net Capacity** - Total days available
- **Feature Dev** - Days allocated for features
- **Bug Fix** - Days allocated for bug fixing

#### 3. **Capacity Distribution**
- Visual cards showing each team member's capacity
- Includes: Available days, Net capacity, Average PF
- Progress bars showing capacity utilization

#### 4. **Team Summary Table**
- Quick overview of all team members
- Columns: Name, Grade, Role, Module Allocation, Avg PF

### Navigating the Dashboard

**Sidebar Navigation:**
- **Dashboard** - Overview and summary
- **KYT** - Team member management
- **Capacity** - Detailed capacity planning
- **Checklist** - Quality gate tracking
- **Guidelines** - Productivity factor reference
- **Configuration** - PI metadata and settings
- **Export Report** - Export and backup options

---

## Know Your Team (KYT)

The KYT section manages all team member information, skills, and certifications.

### Adding a Team Member

#### Required Fields:
1. **Name** - Team member's full name
2. **Grade** - Select from: A, B, C, D, E, F
3. **Role** - Select from: Architect, Tech Lead, Developer, Tester
4. **Overall Experience** - Low (1-3 yrs), Medium (3-5 yrs), High (5+ yrs)

#### Optional Fields:
5. **Technologies & Experience** - Free text field
   - Example: "C++: 5yrs, Python: 3yrs, AUTOSAR: 2yrs"
   - List all relevant technologies with years of experience

6. **Certifications** (Yes/No dropdowns):
   - **Safety Certified** - Safety training completion
   - **Cybersec Trained** - Cybersecurity training status
   - **Project Training Done** - Project-specific training
   - **Delivered Code** - Has delivered production code

7. **% Allocation** - Resource allocation percentage (1.0 = 100%, 0.5 = 50%)

8. **Sprint Performance Factors (S1-S6)**
   - Default: 0.95 for each sprint
   - Adjust based on individual performance expectations
   - Use "T" for training sprints (member in learning mode)

### Team Members Display

**Card-Based Layout:**
- Each member displayed in a professional card
- **Header:** Name, Grade, Role, Experience
- **Technologies:** Listed with wrench icon
- **Key Metrics:** Allocation % and Average PF
- **Certifications:** Color-coded badges (✓ = Yes/Green, × = No/Orange)
- **Sprint Grid:** S1-S6 values with color coding
- **Actions:** Edit and Remove (×) buttons

### Editing Team Members

1. Click **Edit** button on any member card
2. Form populates with current data
3. Modify as needed
4. Click **Add Member** (button changes from "Add" to confirm edit)
5. Click **Cancel** to abort changes

### Removing Team Members

1. Click **× button** on member card
2. Member is immediately removed
3. Capacity data for that member is also removed
4. Changes auto-save

---

## Capacity Planning

The Capacity section provides detailed capacity calculations for each team member.

### Individual Capacity Configuration

#### Access:
- Navigate to **Capacity** tab
- Select team member from dropdown
- View/edit their specific parameters

#### Parameters:

**1. Work Days:**
- **Weeks in PI** - Number of weeks in the PI (default: 12)
- **Saturdays** - Number of working Saturdays (default: 0)
- **Holidays** - Public holidays in the PI period (default: 3)

**2. Leave & Availability:**
- **Leaves** - Planned leave days (default: 7)
- **Misc Days** - Other unavailability (meetings, admin work) (default: 7)
- **% Allocation** - Percentage allocated to this PI (1.0 = 100%)

**3. Training Days:**
- **Pre-PI** - Pre-PI planning/prep days (default: 0)
- **All Hands** - All-hands meeting days (default: 0.18)
- **Competency** - Competency building days (default: 2)
- **GNC** - General/Necessary/Compliance training (default: 1)
- **Others** - Additional training (default: 0)

### Capacity Calculation Formula

```
Weekdays = Weeks × 5
Gross Days = Weekdays + Saturdays
Unavailable = Holidays + Leaves + Misc Days
Training Total = Pre-PI + All Hands + Competency + GNC + Others
Available Days = (Gross Days - Unavailable - Training Total) × Allocation %
Net Capacity = Available Days × Average PF
```

### Capacity Matrix

**Interactive Matrix View:**
- **Rows:** Different capacity parameters
- **Columns:** Team members
- **Totals:** Automatic summations at the row end
- **Excel Compatible:** Same format as traditional templates

**Features:**
- Horizontal scrollbar for many team members
- Color-coded sections for easy reading
- Auto-calculated totals
- Synced with KYT allocation percentages

### Training Days Breakdown

**Editable Table:**
- Click any cell to edit
- Press Enter or click away to save
- Categories: Pre-PI, All Hands, Competency, GNC, Others
- Immediately reflects in capacity calculations

### Automatic Synchronization

When you change **Allocation %** in:
- **KYT tab** → Updates in Capacity tab
- **Capacity tab** → Updates in KYT tab

This ensures consistency across the dashboard!

---

## Checklist

A comprehensive **22-point quality checklist** to ensure your PI plan meets all requirements.

### Checklist Categories

1. **General** (1 item) - Formatting compliance
2. **KYT** (3 items) - Team member data quality
3. **PI Capacity** (2 items) - Capacity calculation accuracy
4. **PI Feature** (9 items) - Feature planning completeness
5. **PI US** (3 items) - User Story quality
6. **Jira** (3 items) - Jira integration readiness

### Using the Checklist

#### Checking Items:
1. Click the **checkbox** next to each item
2. ✓ appears when checked
3. Progress updates automatically
4. Completion percentage shown at top

#### Adding Comments:
1. Each item has a **comment field** below it
2. Click to type justification or notes
3. Use cases:
   - **Not Checked:** "N/A - No external dependencies in this PI"
   - **Additional Context:** "Verified with PO on 03/25/2026"
   - **Delayed Items:** "Pending customer input, due by EOD 03/30"
4. Press Enter or click away to auto-save

#### Progress Tracking:
- **Completed** stat card shows: X/22 items
- **Progress** shows percentage with visual bar
- Helps ensure nothing is missed before submission

### Export Checklist Data

Checklist items and comments are included in:
- **Complete Backup CSV** - For archival
- **CSV Import** - Restore with comments intact

---

## Guidelines

Reference section for **Productivity Factor (PF)** guidelines.

### When to Use This Section

- Setting sprint PF values for new team members
- Adjusting PF based on scenario changes
- Reviewing standard productivity benchmarks

### Productivity Scenarios

The guidelines table provides PF recommendations for various scenarios:
- New joiners vs. experienced members
- Training periods vs. delivery sprints
- Different role types and experience levels
- Special circumstances (PIP, shared resources, etc.)

**Note:** These are guidelines. Adjust PF values based on your team's specific context and historical data.

---

## Configuration

The Configuration section stores all PI metadata and project settings.

### Required Fields (Validated Before Export)

1. **PI Name** - Program Increment identifier
   - Example: "PI-CY26-Q1", "PI-2026-1"
   - Used in all export filenames

2. **Project** - Project name
   - Example: "Qorix Developer", "ADAS Platform"
   - Used in dashboard subtitle and exports

3. **Module/Team Name** - Specific module or team identifier
   - Example: "TeamA", "Perception Module", "Backend Services"
   - Included in exports for clarity

4. **Date** - PI plan creation/approval date
   - Use date picker for consistency

5. **PPM** - Project Program Manager name

6. **PO** - Product Owner name

7. **Scrum Master** - Scrum Master name

8. **Author** - Person who created the PI plan

### Optional Fields

9. **Config ID** - Internal tracking ID (optional)

10. **Version** - Document version (default: "1.0.0")

11. **Status** - Select from dropdown:
    - **Draft** - Initial planning phase (Orange indicator)
    - **In-Review** - Under review (Orange indicator)
    - **Approved** - Approved by stakeholders (Green indicator)
    - **Active** - Currently executing (Blue indicator)

### Settings

12. **Feature Split %** - Percentage for feature development (default: 95%)
    - Remaining % auto-calculated for bug fixing

13. **Sprints** - Number of sprints in PI (default: 6)

### Real-time Status Updates

- When you change **Status** dropdown, the header status indicator updates immediately
- No need to click "Save Configuration" for status changes
- Other fields require clicking "Save Configuration"

### How Configuration Affects Exports

- **PDF Export:** Uses PI name as document title
- **All CSV/JSON Exports:** Include PI, Project, Module in filename
- **Dashboard Subtitle:** Shows "PI · Project · Module/Team"
- **Capacity Matrix:** Headers show PI name

---

## Export & Reporting

Multiple export options for sharing and archiving your PI plan.

### Export Options

#### 1. **Download Data (JSON)**
**Purpose:** Raw data export for backup or integration

**Filename Format:** `[PI Name]-[Project]-[Module/Team]-[Date].json`

**Example:** `PI-CY26-Q1-Qorix-Developer-TeamA-2026-03-25.json`

**Contains:**
- Complete state object
- All configuration
- All team members
- All capacity data
- Checklist with comments
- Human-readable JSON format

**Use Cases:**
- Full backup before major changes
- Data migration to other tools
- Development/integration purposes

---

#### 2. **Export Capacity Matrix (CSV)**
**Purpose:** Excel-compatible capacity matrix

**Filename Format:** `[PI Name]-[Project]-[Module/Team]-Capacity.csv`

**Example:** `PI-CY26-Q1-Qorix-Developer-TeamA-Capacity.csv`

**Contains:**
- Horizontal capacity matrix
- Team member names and roles
- All capacity parameters
- Training breakdown
- Calculated totals
- Excel-compatible format

**Use Cases:**
- Sharing with stakeholders who prefer Excel
- Creating presentations
- Detailed capacity analysis
- Matching traditional Excel template format

---

#### 3. **Print Dashboard to PDF**
**Purpose:** Professional PDF report of complete dashboard

**Filename Format:** `[PI Name] - [Project] - [Module/Team].pdf`

**Example:** `PI-CY26-Q1 - Qorix Developer - TeamA.pdf`

**How to Use:**
1. Click "Print Dashboard to PDF" button
2. Print dialog opens
3. Select **"Save as PDF"** or **"Microsoft Print to PDF"** as destination
4. Click **Save**
5. Choose location and confirm

**Contains:**
- PI Plan title and subtitle
- All 4 statistics cards
- Capacity distribution cards for each member
- Team summary table
- Professional formatting for printing

**Use Cases:**
- Stakeholder presentations
- PI plan submissions
- Archival in PDF format
- Sharing via email

---

#### 4. **Copy to Clipboard**
**Purpose:** Quick text-based report for emails/chat

**Format:** Plain text with ASCII art formatting

**Contains:**
- PI configuration summary
- Dashboard overview
- Team members list
- Capacity breakdown
- Capacity allocation
- Quality checklist progress
- Timestamp

**Use Cases:**
- Quick sharing in emails
- Pasting into chat messages (Slack, Teams)
- Adding to Confluence pages
- Text-based documentation

---

### Backup & Restore (CSV)

#### **Download Complete Backup (CSV)**

**Purpose:** Complete data backup for editing in Excel and restoration

**Filename Format:** `[PI Name]-[Project]-[Module/Team]-Backup-[Date].csv`

**Example:** `PI-CY26-Q1-Qorix-Developer-TeamA-Backup-2026-03-25.csv`

**Contains 4 Sections:**

1. **### CONFIGURATION ###**
   - All configuration fields (PI name, project, dates, etc.)

2. **### TEAM MEMBERS (KYT) ###**
   - All team member details
   - Technologies, certifications
   - Sprint PF values

3. **### CAPACITY DETAILS ###**
   - Individual capacity parameters for each member
   - Training days breakdown

4. **### CHECKLIST ###**
   - Checklist items
   - Checked status (Yes/No)
   - Comments/justifications

**Use Cases:**
- Regular backups before major changes
- Editing data in Excel (bulk updates)
- Sharing complete plan with other teams
- Archiving PI plans for future reference

---

#### **Upload CSV Backup**

**Purpose:** Restore data from a previously saved backup

**How to Use:**
1. Click "Upload CSV Backup" button
2. File picker opens
3. Select your CSV backup file
4. Click Open
5. Data imports and dashboard updates

**Important Notes:**
- Must be in the correct CSV backup format
- Overwrites current data (backup first if needed!)
- Validates file structure during import
- Shows success/error message

**Supported Format:**
- Only CSV files created by "Download Complete Backup"
- Must have section headers (### CONFIGURATION ###, etc.)
- Quoted values supported
- Empty lines ignored

---

### Export Validation

**All exports require complete configuration!**

Before any export, the dashboard validates that these fields are filled:
- PI Name ✓
- Project ✓
- Module/Team Name ✓
- Date ✓
- PPM ✓
- PO ✓
- Scrum Master ✓
- Author ✓

If any field is missing, you'll see an alert:
```
⚠️ Configuration Incomplete

Please fill in the following required fields in Configuration tab:

• [Missing Field 1]
• [Missing Field 2]
...

Go to Configuration tab to complete these fields before exporting.
```

**Why?** This ensures exported files have complete metadata and professional appearance.

---

## Data Management

### Auto-Save

**Your data is automatically saved to browser storage!**

**When does it save?**
- Adding/editing/removing team members
- Changing capacity parameters
- Updating configuration
- Checking/unchecking checklist items
- Adding checklist comments
- Switching between team members in capacity view

**Where is it saved?**
- Browser's localStorage (IndexedDB)
- Specific to the browser and computer
- Survives browser restarts
- ~2MB storage capacity

**Limitations:**
- Data is local to one browser on one computer
- Clearing browser data deletes saved state
- Incognito/Private mode doesn't persist data
- Different browsers = different storage

---

### Reset Dashboard

**Fresh start for a new PI plan**

**Button Location:** Header (top right) - Red "⟲ Reset" button

**What happens:**
1. Confirmation dialog with warning
2. All data cleared:
   - All team members removed
   - Capacity data deleted
   - Configuration reset to defaults
   - Checklist cleared
   - Browser storage cleared
3. Returns to empty template state
4. Navigates to Configuration tab

**Safety Features:**
- Requires confirmation (can't accidentally reset)
- Shows detailed warning of what will be lost
- Suggests downloading backup first

**Use Cases:**
- Starting a new PI plan
- Switching to a different project
- Testing/demo purposes
- Recovering from errors

---

### Data Persistence Strategy

**Recommended Workflow:**

1. **Daily:** Rely on auto-save for ongoing work

2. **Weekly:** Download complete CSV backup
   - Store in shared drive
   - Name with date: `PI-CY26-Q1-Backup-2026-03-25.csv`

3. **Milestones:** Export PDF for archival
   - Draft completion
   - Approval
   - Final version

4. **Before Major Changes:**
   - Download backup
   - Make changes
   - If issues: Upload old backup to restore

5. **Shared Planning:**
   - One person: Download backup CSV
   - Share file with others
   - Others: Upload CSV to their browser
   - Everyone works with same data

---

## Best Practices

### 1. Configuration Setup

**✓ DO:**
- Fill all required fields completely
- Use consistent naming conventions (e.g., "PI-CY26-Q1" not "PI CY26 Q1")
- Set realistic feature/bug split percentages
- Update date field when plan changes

**✗ DON'T:**
- Leave default values like "PI-YYYY-QX" or "Project Name"
- Use special characters that don't work in filenames
- Forget to click "Save Configuration" after changes

---

### 2. Team Member Management

**✓ DO:**
- Add complete technology information (helps with skill mapping)
- Set realistic sprint PF values based on historical data
- Update certifications when team members complete training
- Use "T" for sprints where member is in full training mode
- Review and update member data each PI

**✗ DON'T:**
- Copy-paste same PF value for all members without thought
- Forget to update allocation % for part-time members
- Leave technology field empty (makes capability planning harder)

---

### 3. Capacity Planning

**✓ DO:**
- Discuss leave plans with individuals before entering
- Account for known holidays in advance
- Budget realistic training days based on plans
- Review training breakdown matches actual needs
- Switch members in capacity dropdown to save changes

**✗ DON'T:**
- Use default values for everyone (customize per person)
- Forget about public holidays in your region
- Over-allocate (keep some buffer for unknowns)
- Ignore the training needs

---

### 4. Checklist Usage

**✓ DO:**
- Review every item systematically
- Add comments for unchecked or N/A items
- Add comments explaining context even for checked items
- Complete checklist before final submission
- Export PDF with complete checklist

**✗ DON'T:**
- Check all boxes without actual verification
- Leave critical items unchecked without explanation
- Skip the checklist (it's there for quality!)

---

### 5. Export & Backup

**✓ DO:**
- Download backup CSV regularly (weekly minimum)
- Export PDF at major milestones
- Use CSV backup before doing bulk changes
- Keep backups in version control or shared drive
- Include date in backup filenames

**✗ DON'T:**
- Rely only on browser storage (data can be lost!)
- Wait until disaster to create first backup
- Overwrite backups (keep versions)

---

### 6. Data Validation

**✓ DO:**
- Validate totals make sense
- Cross-check capacity vs. available work
- Review that sum of allocations = available team capacity
- Verify sprint PF values are reasonable (0.7-0.95 typical range)
- Check that training days + work days don't exceed calendar days

**✗ DON'T:**
- Assume calculations are always correct
- Skip sanity checks on totals
- Ignore warnings or unusual numbers

---

## Troubleshooting

### Issue: Data Not Saving

**Symptoms:** Changes disappear after refresh

**Causes & Solutions:**

1. **Browser in Private/Incognito Mode**
   - Solution: Use normal browser mode for persistent storage

2. **Browser Storage Disabled**
   - Solution: Check browser settings → Privacy → Allow local storage

3. **Storage Quota Exceeded**
   - Solution: Clear old browser data or use a different browser

4. **Browser Extension Blocking**
   - Solution: Disable adblockers/privacy extensions for this page

---

### Issue: Print Dialog Not Opening

**Symptoms:** Click "Print Dashboard to PDF", nothing happens

**Causes & Solutions:**

1. **Pop-up Blocker**
   - Solution: Allow pop-ups for this page in browser settings

2. **Browser Permission Denied**
   - Solution: Grant print permissions when browser asks

3. **Keyboard Shortcut Alternative**
   - Solution: Use Ctrl+P (Windows) or Cmd+P (Mac)
   - Navigate to Dashboard first
   - Then press print shortcut
   - Select "Save as PDF"

---

### Issue: CSV Import Fails

**Symptoms:** Upload CSV shows error or doesn't import

**Causes & Solutions:**

1. **Wrong CSV Format**
   - Solution: Only import CSV files created by "Download Complete Backup"
   - Don't edit the section headers (### CONFIGURATION ###, etc.)

2. **Excel Modified the Format**
   - Solution: When saving in Excel, use "CSV UTF-8" format
   - Ensure special characters are preserved

3. **Incomplete CSV**
   - Solution: Check that all sections are present
   - Compare with a working backup file

---

### Issue: Capacity Calculations Wrong

**Symptoms:** Net capacity doesn't match expectations

**Causes & Solutions:**

1. **Sprint PF Values**
   - Check: Review S1-S6 values for the member
   - Average PF is calculated across all 6 sprints

2. **Training Days High**
   - Check: Review training breakdown
   - Pre-PI + All Hands + Competency + GNC + Others

3. **Allocation Percentage**
   - Check: Verify % Allocation is correct (1.0 = 100%, 0.5 = 50%)

4. **Sync Issue**
   - Solution: Switch to another member and back in capacity dropdown
   - This triggers recalculation

---

### Issue: Module Name Not Showing in Exports

**Symptoms:** Filename or PDF doesn't include module/team name

**Causes & Solutions:**

1. **Module Field Empty**
   - Solution: Fill "Module/Team Name" in Configuration tab
   - Click "Save Configuration"

2. **Not Refreshed**
   - Solution: Navigate to Dashboard after saving config
   - Then export again

---

### Issue: Team Members Not Appearing

**Symptoms:** Added team member doesn't show in list

**Causes & Solutions:**

1. **Form Not Submitted**
   - Solution: Ensure you clicked "Add Member" button
   - Watch for success toast notification

2. **Name Field Empty**
   - Solution: Name is required - fill it in

3. **Page Not Refreshed**
   - Solution: Click on another tab and back to KYT

---

### Issue: Browser Compatibility

**Symptoms:** Dashboard looks broken or doesn't work

**Causes & Solutions:**

1. **Old Browser Version**
   - Solution: Update to latest browser version
   - Chrome 90+, Edge 90+, Firefox 88+, Safari 14+

2. **JavaScript Disabled**
   - Solution: Enable JavaScript in browser settings

3. **File Not Fully Loaded**
   - Solution: Ensure the entire HTML file downloaded
   - Check file size is reasonable (~150-200KB)

---

## FAQ

### General Questions

**Q: Do I need internet to use this?**
A: No! After opening the file once, it works completely offline. All data is stored locally in your browser.

**Q: Can multiple people work on the same PI plan simultaneously?**
A: Not in real-time. Use this workflow:
1. One person maintains the master plan
2. Export CSV backup
3. Share CSV file
4. Others import it to their browser
5. Consolidate changes back to master

**Q: Is my data secure?**
A: Yes! All data stays on your computer in your browser. Nothing is sent to any server. You maintain complete control and privacy.

**Q: Can I use this on my tablet or phone?**
A: The dashboard works on tablets. Phone screens are too small for optimal experience. Desktop/laptop recommended.

---

### Data & Storage

**Q: How much data can I store?**
A: Browser localStorage typically provides 5-10MB. This dashboard uses ~2MB maximum, enough for large teams (50+ members).

**Q: What happens if I clear my browser cache?**
A: Your PI plan data will be lost! Always maintain CSV backups for important plans.

**Q: Can I transfer my plan to another computer?**
A: Yes! Download CSV backup → Transfer file → Upload on other computer.

**Q: How do I recover if I accidentally delete data?**
A: If you have a CSV backup, upload it. Otherwise, data cannot be recovered. Always maintain backups!

---

### Features & Usage

**Q: Why can't I export if configuration is incomplete?**
A: To ensure all exported files have proper metadata and look professional with complete information.

**Q: Can I customize the checklist items?**
A: Currently no. The 22 items cover standard PI planning requirements. You can add comments for custom needs.

**Q: How do I handle team members joining mid-PI?**
A: Add them with appropriate sprint PF values. Set "T" for sprints before they join, normal values after.

**Q: What does "T" mean for sprint PF?**
A: "T" = Training. Use when a team member is in learning mode for that sprint (typically new joiners or skill transitions).

**Q: Can I track dependencies in this tool?**
A: Not directly. Use the checklist comment field to note dependencies, or track in your backlog management tool (Jira).

---

### Exports

**Q: Why is my PDF filename different from what I expected?**
A: Filenames use PI Name, Project, and Module/Team from Configuration. Update those fields to change export names.

**Q: Can I edit the exported CSV in Excel?**
A: Yes! The "Export Capacity Matrix" CSV is Excel-compatible. Edit and share.

**Q: What's the difference between capacity CSV and backup CSV?**
A: 
- **Capacity CSV:** Matrix view for stakeholders, Excel-compatible
- **Backup CSV:** Complete data for restoration, includes checklist & comments

**Q: How do I get a PDF if print doesn't work?**
A: 
1. Use Ctrl+P (Windows) or Cmd+P (Mac)
2. Select "Save as PDF" as destination
3. Or use browser's built-in PDF export feature

---

### Technical

**Q: What technology is this built with?**
A: Pure HTML, CSS, and JavaScript. No frameworks, no dependencies, no server needed.

**Q: Can I modify the HTML file?**
A: Yes, it's yours! Edit as needed. Keep a backup of the original.

**Q: Can I integrate this with other tools?**
A: Yes! Use JSON export format. The data structure is documented in the JSON file itself.

**Q: Does this work in all browsers?**
A: Works in all modern browsers (Chrome, Edge, Firefox, Safari). Internet Explorer is not supported.

---

### Workflow

**Q: What's the recommended workflow for a PI planning session?**
A:
1. Pre-Planning: Configure PI details
2. Day 1: Add team members, set capacities
3. Day 2: Review checklist, adjust PF values
4. Day 3: Finalize, export PDF, backup CSV
5. Submission: Share PDF with stakeholders
6. Archive: Store backup CSV in shared drive

**Q: How often should I backup?**
A: 
- Daily during active planning
- Weekly during PI execution
- Before any major changes
- Before browser updates/maintenance

**Q: Should I use JSON or CSV for backups?**
A: CSV backup is recommended:
- Human-readable
- Editable in Excel
- Includes everything (config, KYT, capacity, checklist)
- Easier to share and review

---

## Support & Feedback

### Need Help?

1. **Read this guide** - Most questions answered here
2. **Check Troubleshooting** - Common issues and solutions
3. **Review FAQ** - Quick answers to frequent questions
4. **Contact Support** - [Insert your support contact]

### Report Issues

If you encounter bugs or issues:
1. Note the steps to reproduce
2. Check browser console for errors (F12 → Console)
3. Include your browser version and OS
4. Contact: [Insert contact email/channel]

### Feature Requests

We welcome suggestions for improvements:
- New features
- UI/UX enhancements
- Export format requests
- Process improvements

Submit ideas to: [Insert feedback channel]

---

## Updates & Changelog

**Current Version:** 1.0.0 (March 2026)

### Version 1.0.0 - Initial Release
- Know Your Team (KYT) management with certifications
- Capacity planning with training breakdown
- 22-point quality checklist with comments
- Multiple export formats (PDF, CSV, JSON)
- Complete backup & restore functionality
- Auto-save and browser storage
- Responsive card-based UI
- Module/Team name support
- Real-time status indicators

---

## Appendix

### Keyboard Shortcuts

- **Ctrl+P / Cmd+P** - Print (alternative to Print button)
- **Tab** - Navigate between form fields
- **Enter** - Submit forms, save editable cells
- **Escape** - Cancel edit mode (where applicable)

### Browser Storage Information

**Data stored in localStorage:**
- Full state object (JSON format)
- Configuration
- Team members
- Capacity data
- Checklist items and comments

**Storage key:** `piPlanState`

**To manually inspect:**
1. Open browser DevTools (F12)
2. Go to Application tab
3. Expand Local Storage
4. Find `piPlanState`

---

## Quick Reference Card

### Essential Workflows

**Start New PI Plan:**
1. Configuration → Fill fields → Save
2. KYT → Add members
3. Capacity → Configure per member
4. Checklist → Review items
5. Export → Download backups

**Daily Updates:**
1. Open index.html
2. Make changes (auto-saves)
3. Download backup CSV (end of day)

**Final Submission:**
1. Complete all checklist items
2. Verify configuration complete
3. Print Dashboard to PDF
4. Download backup CSV
5. Share PDF with stakeholders

**Restore from Backup:**
1. Export → Upload CSV Backup
2. Select backup file
3. Confirm import

---

**End of User Guide**

For additional support, contact: [Your Support Channel]

**Document Version:** 1.0.0  
**Last Updated:** March 2026  
**Author:** [Your Name/Team]
