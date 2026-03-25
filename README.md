# PI Planning Capacity Dashboard

> A comprehensive, browser-based PI Planning tool for team capacity management and resource tracking

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Browser](https://img.shields.io/badge/browser-Chrome%20%7C%20Edge%20%7C%20Firefox%20%7C%20Safari-green)
![License](https://img.shields.io/badge/license-Internal%20Use-orange)

---

## 🚀 Quick Start

1. **Open** `index.html` in any modern web browser
2. **Configure** your PI details in the Configuration tab
3. **Add** team members in the KYT (Know Your Team) tab
4. **Plan** capacity for each team member
5. **Export** your plan as PDF, CSV, or JSON

**No installation required. No server needed. Works offline!**

---

## ✨ Features

### 📊 Dashboard Overview
- Real-time team capacity summary
- Visual capacity distribution cards
- Team statistics at a glance
- Professional status indicators

### 👥 Know Your Team (KYT)
- Team member management with detailed profiles
- Technology and experience tracking
- Certification monitoring (Safety, Cybersecurity, Training, Code Delivery)
- Sprint performance factor configuration (S1-S6)
- Allocation percentage tracking

### 📈 Capacity Planning
- Individual capacity configuration per team member
- Automated capacity calculations
- Training days breakdown (Pre-PI, All Hands, Competency, GNC, Others)
- Horizontal matrix view (Excel-compatible)
- Real-time synchronization with KYT data

### ✅ Quality Checklist
- 22-point comprehensive review checklist
- Categories: General, KYT, PI Capacity, PI Feature, PI US, Jira
- Comment fields for justification/notes
- Progress tracking

### ⚙️ Configuration Management
- PI metadata (PI Name, Project, Module/Team)
- Document tracking (Version, Date, Status)
- Stakeholder information (PPM, PO, Scrum Master, Author)
- Feature/Bug split configuration

### 📤 Export & Reporting
- **Print to PDF** - Complete dashboard export
- **Capacity Matrix CSV** - Excel-compatible format
- **Complete Backup CSV** - Full data with comments
- **JSON Export** - Raw data for integration
- **Copy to Clipboard** - Quick text report
- **Professional file naming** - Includes PI, Project, Module in all exports

### 💾 Data Management
- Auto-save to browser storage
- CSV backup and restore
- Reset functionality
- Import/Export capabilities

---

## 📋 Requirements

- **Browser:** Chrome 90+, Edge 90+, Firefox 88+, or Safari 14+
- **Storage:** ~2MB browser local storage
- **Internet:** Not required (works offline)
- **OS:** Windows, macOS, or Linux

---

## 📖 Documentation

### For Users
- **[USER-GUIDE.md](USER-GUIDE.md)** - Comprehensive user guide with tutorials, best practices, and troubleshooting
- **[ANNOUNCEMENT-EMAIL.md](ANNOUNCEMENT-EMAIL.md)** - Sample announcement email template

### Quick Links
- [Getting Started](#quick-start)
- [Features Overview](#features)
- [Troubleshooting](USER-GUIDE.md#troubleshooting)
- [FAQ](USER-GUIDE.md#faq)

---

## 🎯 Usage Workflow

### Initial Setup (5 minutes)
```
1. Open index.html in browser
2. Navigate to Configuration tab
3. Fill in required fields (PI Name, Project, Module/Team, etc.)
4. Click "Save Configuration"
```

### Adding Team Members
```
1. Go to KYT tab
2. Fill in team member details (Name, Grade, Role, Experience)
3. Add technologies and certifications
4. Set sprint performance factors (S1-S6)
5. Click "Add Member"
```

### Capacity Planning
```
1. Navigate to Capacity tab
2. Select team member from dropdown
3. Configure work days, leaves, training days
4. Review capacity matrix
5. Changes auto-save
```

### Export Your Plan
```
1. Complete all required configuration fields
2. Review checklist
3. Go to Export Report tab
4. Choose export format:
   - Print Dashboard to PDF (for stakeholders)
   - Export Capacity Matrix CSV (for Excel editing)
   - Download Complete Backup CSV (for archival)
```

---

## 💡 Key Concepts

### Sprint Performance Factor (PF)
- Represents expected productivity for each sprint (0.0 to 1.0)
- Typical range: 0.70 - 0.95
- Use "T" for training sprints
- Average PF calculated across all 6 sprints

### Capacity Calculation
```
Gross Days = (Weeks × 5) + Saturdays
Available Days = (Gross Days - Holidays - Leaves - Misc Days - Training Days) × Allocation %
Net Capacity = Available Days × Average PF
```

### Training Days Breakdown
- **Pre-PI:** Pre-PI planning and preparation
- **All Hands:** All-hands meetings
- **Competency:** Competency building activities
- **GNC:** General/Necessary/Compliance training
- **Others:** Additional training needs

---

## 🔒 Data Privacy & Security

- ✅ All data stored locally in your browser
- ✅ No data sent to any server
- ✅ You maintain complete control
- ✅ Works completely offline
- ⚠️ Backup regularly (CSV export) - browser data can be cleared

---

## 📊 Export File Naming Convention

All exports use a consistent, professional naming pattern:

**Format:** `[PI Name]-[Project]-[Module/Team]-[Type]-[Date]`

**Examples:**
- PDF: `PI-CY26-Q1 - Qorix Developer - TeamA.pdf`
- JSON: `PI-CY26-Q1-Qorix-Developer-TeamA-2026-03-25.json`
- Capacity CSV: `PI-CY26-Q1-Qorix-Developer-TeamA-Capacity.csv`
- Backup CSV: `PI-CY26-Q1-Qorix-Developer-TeamA-Backup-2026-03-25.csv`

---

## ❓ FAQ

**Q: Do I need internet to use this?**  
A: No! It works completely offline after opening the file once.

**Q: Is my data secure?**  
A: Yes! All data stays on your computer. Nothing is sent to any server.

**Q: Can multiple people work on the same plan?**  
A: Share the CSV backup file. Others can import it to their browser.

**Q: How do I backup my data?**  
A: Go to Export Report tab → Download Complete Backup (CSV). Do this regularly!

**Q: What if I clear my browser cache?**  
A: Data will be lost. Always maintain CSV backups!

**Q: Can I edit the exported CSV in Excel?**  
A: Yes! The Capacity Matrix CSV is fully Excel-compatible.

---

## 🛠️ Troubleshooting

### Print to PDF Not Working
1. Check browser allows pop-ups
2. Try keyboard shortcut: Ctrl+P (Windows) or Cmd+P (Mac)
3. Select "Save as PDF" from printer dropdown

### Data Not Saving
1. Ensure not in private/incognito mode
2. Check browser allows local storage
3. Verify storage quota not exceeded

### CSV Import Fails
1. Only import CSV files created by "Download Complete Backup"
2. Don't modify section headers (### CONFIGURATION ###)
3. Save as "CSV UTF-8" if edited in Excel

See [Troubleshooting Guide](USER-GUIDE.md#troubleshooting) for more solutions.

---

## 📞 Support

- **Documentation:** [USER-GUIDE.md](USER-GUIDE.md)
- **Issues:** [Insert your issue tracking system]
- **Questions:** [Insert your support channel]
- **Feedback:** [Insert your feedback channel]

---

## 🎓 Best Practices

**Daily:**
- ✅ Make changes (auto-saves to browser)
- ✅ Review team member allocations

**Weekly:**
- ✅ Download CSV backup
- ✅ Store in shared drive or version control

**Milestones:**
- ✅ Export PDF for stakeholder review
- ✅ Complete checklist items with comments
- ✅ Verify all configuration fields filled

**Before Major Changes:**
- ✅ Download backup CSV first
- ✅ Make changes
- ✅ If needed, restore from backup

---

## 📝 Changelog

### Version 1.0.0 (March 2026)
- Initial release
- KYT management with 4 certification fields
- Capacity planning with training breakdown
- 22-point quality checklist with comments
- Multiple export formats (PDF, CSV, JSON)
- Complete backup & restore
- Auto-save functionality
- Module/Team name support
- Professional file naming
- Real-time status indicators

---

## 📄 File Structure

```
PI_PlanDashboard/
├── index.html              # Main application (open this!)
├── README.md               # This file
├── USER-GUIDE.md           # Comprehensive user guide
└── ANNOUNCEMENT-EMAIL.md   # Sample announcement email
```

---

## 🚦 Status Indicators

The dashboard header shows real-time status with color coding:

- **Draft** 🟠 - Initial planning phase
- **In-Review** 🟠 - Under review by stakeholders
- **Approved** 🟢 - Approved and ready
- **Active** 🔵 - Currently executing

Change status in Configuration tab → Status dropdown.

---

## 💻 Technology Stack

Built with pure web technologies:
- **HTML5** - Structure
- **CSS3** - Styling (Dark theme, responsive design)
- **Vanilla JavaScript** - Functionality (No frameworks!)
- **LocalStorage** - Data persistence
- **Google Fonts** - Typography (DM Mono, Syne)

**No build process. No dependencies. Just open and use!**

---

## 🎯 Use Cases

✅ **PI Planning Sessions** - Complete team capacity planning  
✅ **Stakeholder Presentations** - Professional PDF exports  
✅ **Resource Management** - Track team member skills and certifications  
✅ **Capacity Tracking** - Monitor availability and allocation  
✅ **Quality Assurance** - Systematic checklist review  
✅ **Data Archival** - CSV backup for historical records  
✅ **Excel Integration** - Export capacity matrix for further analysis  

---

## 🔄 Updates

Check for updates periodically. Current version shows in Configuration tab.

To upgrade:
1. Download complete backup CSV
2. Replace index.html with new version
3. Open new version
4. Upload backup CSV to restore data

---

## 📜 License

Internal use only. All rights reserved.

---

## 🙏 Acknowledgments

Designed for efficient PI planning and team capacity management.

Built with ❤️ for engineering teams.

---

**Ready to start?** Open `index.html` and begin planning your next PI!

For detailed instructions, see **[USER-GUIDE.md](USER-GUIDE.md)**
