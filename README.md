# SCT Maker - Self-Assessment Tool Builder

> A powerful, interactive tool for creating customizable self-assessment checklists for Specialized Care Teams (SCT), Medical Emergency Teams (EMT), and similar organizations.

[![Version](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/yourusername/sct-maker)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Maker Interface](#maker-interface)
- [Generated Assessment Tool](#generated-assessment-tool)
- [Advanced Features](#advanced-features)
- [Save & Load Functionality](#save--load-functionality)
- [Rich Text Editor](#rich-text-editor)
- [Deployment Modalities](#deployment-modalities)
- [Export Options](#export-options)
- [Tips & Best Practices](#tips--best-practices)
- [Troubleshooting](#troubleshooting)
- [Technical Details](#technical-details)

---

## 🎯 Overview

The SCT Maker is a standalone HTML tool that allows you to:

1. **Build** custom assessment tools with configurable sections and standards
2. **Customize** content, weights, and deployment modalities
3. **Generate** fully functional HTML assessment tools
4. **Save** and share your work with complete data preservation

**No installation required** - Just open the HTML file in any modern browser!

---

## ✨ Features

### 🎨 Maker (Tool Builder)

- ✅ **Dynamic Section Management**
  - Create, delete, and reorder sections
  - Assign custom weights to sections
  - Enable/disable sections on the fly

- ✅ **Flexible Content Editing**
  - Rich text editor with formatting options
  - Insert tables with resize capability
  - Add hyperlinks to external resources
  - Collapse/expand standards for easy navigation

- ✅ **Drag & Drop Interface**
  - Reorder sections
  - Reorder standards within sections
  - Visual feedback during dragging

- ✅ **Deployment Modalities**
  - Support for multiple deployment profiles (Embedded, Coupled, Self-Sustained)
  - Customizable requirements per modality
  - Mitigation strategies for each profile

- ✅ **State Management**
  - Save entire maker configuration as HTML
  - Load previously saved configurations
  - Auto-restore on file open

### 🔧 Generated Assessment Tool

- ✅ **Interactive Assessment**
  - Collapsible standards with color-coded status
  - Evidence, Gaps, and Actions tracking
  - Compliance scoring (0-3, N/A)
  - Real-time progress calculation

- ✅ **Data Persistence**
  - Auto-save to localStorage
  - Export as HTML with all data
  - Export to Excel
  - Export to JSON
  - Generate PDF reports

- ✅ **User-Friendly Interface**
  - Responsive design (desktop, tablet, mobile)
  - Dark mode support
  - Progress tracking sidebar
  - Visual progress indicators

---

## 🚀 Getting Started

### Quick Start

1. **Download** the `index.html` file
2. **Open** in your browser (Chrome, Firefox, Edge, Safari)
3. **Start building** your assessment tool

### Basic Workflow

```
1. Configure Sections
   └─> Add/remove sections
   └─> Set section weights (must total 100%)
   └─> Enable/disable sections

2. Add Standards
   └─> Create standards within sections
   └─> Add descriptions using rich text editor
   └─> Organize with drag & drop

3. Select Deployment Modalities
   └─> Choose supported deployment profiles
   └─> Configure requirements per modality

4. Generate Tool
   └─> Click "Generate Complete HTML Tool"
   └─> Save the generated assessment tool

5. Use Assessment Tool
   └─> Open generated HTML file
   └─> Complete assessments
   └─> Save progress
   └─> Export reports
```

---

## 🎨 Maker Interface

### Section Management

#### Creating Sections

**Default Sections:**
- INFO
- DEFINITION
- ORGANIZATIONAL DETAIL
- GUIDING PRINCIPLES
- CORE STANDARDS
- CLINICAL STANDARDS
- LOGISTIC STANDARDS
- WASH STANDARDS
- REGULATIONS
- STAFFING & TRAINING
- SUMMARY

**Create Custom Section:**

1. Click **"Create New Section"** button
2. Fill in the form:
   - **Section Key**: Unique identifier (e.g., `clinical-standards`)
   - **Section Title**: Display name (e.g., `CLINICAL STANDARDS`)
   - **Icon**: FontAwesome class (e.g., `fa-stethoscope`)
   - **Weight**: Percentage (0-100)
   - **Has Subsections**: Yes/No
   - **Subsections**: List of standards (one per line)
3. Click **"Create Section"**

#### Managing Sections

**Drag & Drop Reordering:**
- Drag the grip icon (⋮⋮) to reorder sections
- Visual feedback shows drop position
- Sections automatically renumber

**Edit Section Weights:**
- Update weight values inline in Section Management panel
- Weights automatically sync across the interface
- Total must equal 100%

**Delete Sections:**
- Click the trash icon next to any section
- Confirm deletion
- Section removed from all views

### Working with Standards

#### Adding Standards

1. Navigate to a section with subsections
2. Click **"Add Standard"** button
3. Standard item appears with:
   - Name input field
   - Rich text editor for content
   - Deployment requirements (if modalities selected)
   - Delete button

#### Editing Standards

**Standard Name:**
- Enter descriptive title
- Updates automatically in collapsed header

**Standard Content:**
- Use rich text editor
- Format text (bold, italic, underline)
- Create lists (bulleted, numbered)
- Insert tables
- Add hyperlinks
- Clear formatting

#### Organizing Standards

**Collapse/Expand:**
- Click standard header to collapse/expand
- Use **"Collapse All"** button to close all standards
- Use **"Expand All"** button to open all standards

**Drag & Drop Reordering:**
- Drag grip icon (⋮⋮) to reorder
- Only within same section
- Indices update automatically

### Deployment Modalities

#### Selecting Modalities

Three deployment profiles available:

1. **Embedded** 🔵
   - Integrated with existing facility
   - Shared resources
   - Lower autonomy

2. **Coupled** 🟡
   - Adjacent to facility
   - Some shared resources
   - Moderate autonomy

3. **Self-Sustained** 🟢
   - Fully independent
   - All resources included
   - Complete autonomy

**How to select:**
- Check/uncheck modality boxes
- Selected modalities appear in:
  - Deployment summary banner
  - Standard requirements sections
  - Generated tool

#### Configuring Requirements

For each standard and selected modality:

**Requirements:**
- What is needed to meet this standard
- Resources, capabilities, procedures

**Mitigations:**
- Alternatives if requirements not met
- Workarounds and adaptations

**Example:**
```
Standard: Water Supply

EMBEDDED MODE
Requirements: Connection to facility water system
Mitigations: Verify water quality, install filters if needed

SELF-SUSTAINED MODE
Requirements: Water purification system, storage tanks (500L min)
Mitigations: Emergency water delivery contract, backup purification
```

---

## 🔧 Generated Assessment Tool

### Interface Overview

```
┌─────────────────────────────────────────────────────┐
│  Sidebar    │   Main Content    │   Progress Panel  │
│             │                   │                   │
│  - Sections │   - Standards     │   - Overall %     │
│  - Progress │   - Evidence      │   - By Section    │
│             │   - Gaps          │   - Status        │
│             │   - Actions       │                   │
│             │   - Scoring       │                   │
└─────────────────────────────────────────────────────┘
```

### Completing Assessments

#### Standards Display

**Collapsed State (Default):**
- Shows standard title
- Shows compliance score badge
- Color-coded by score:
  - 🔴 Red: Not Started (0)
  - 🟠 Orange: Initial (1)
  - 🟡 Yellow: In Progress (2)
  - 🟢 Green: Completed (3)
  - ⚪ Gray: N/A

**Expanded State:**
- Full standard description
- Deployment requirements (if applicable)
- Input fields:
  - **Evidence**: Describe what you have
  - **Gaps**: What's missing
  - **Actions**: What needs to be done
- **Compliance Score** dropdown

#### Scoring System

| Score | Label | Meaning |
|-------|-------|---------|
| 0 | Not Started | No work begun |
| 1 | Initial | Planning phase, some preparation |
| 2 | In Progress | Actively working, partial completion |
| 3 | Completed | Fully implemented and operational |
| N/A | Not Applicable | Does not apply to this team |

#### Progress Tracking

**Overall Completion:**
- Weighted average across all sections
- Displayed as percentage
- Updates in real-time

**Section Progress:**
- Individual section completion
- Weighted contribution to overall score
- Visible in progress sidebar

### Data Management

#### Auto-Save

- Automatic save to browser localStorage
- Saves every time you change a field
- No manual save needed
- Data persists between sessions

#### Manual Save

**Save Draft Button:**
- Saves current state
- Shows confirmation message
- Data stored in localStorage

**Important:** localStorage is browser-specific. If you clear browser data, your progress is lost. Use export features for backups!

---

## 🌟 Advanced Features

### Section Management (Maker)

#### Dynamic Weights

**Update on the Fly:**
1. Navigate to **Section Management** panel
2. Change weight value in inline input
3. Value syncs to weight assignment section
4. Total weight sum updates automatically

**Validation:**
- Sum must equal 100%
- Alert shown if not valid:
  - Red: Sum ≠ 100%
  - Green: Sum = 100%

#### Collapse/Expand Interface

**Benefits:**
- Reduce visual clutter
- Easy navigation with many standards
- Quick reorganization
- Focus on specific standards

**Controls:**
- **Individual**: Click standard header
- **Bulk**: Use "Collapse All" / "Expand All" buttons
- **Keyboard**: Tab through collapsed standards

### Rich Text Editor

#### Formatting Options

**Text Formatting:**
- **Bold** (`Ctrl+B` compatible)
- *Italic* (`Ctrl+I` compatible)
- <u>Underline</u> (`Ctrl+U` compatible)

**Lists:**
- Bulleted lists
- Numbered lists
- Nested lists (indent/outdent)

**Tables:**
- Custom dimensions (1-20 rows, 1-10 columns)
- Editable cells
- Resizable (drag corner)
- Header row styling

**Hyperlinks:**
- Insert links to external resources
- Edit existing links
- Remove links
- Links open in new tab

**Clear Formatting:**
- Remove all formatting
- Convert to plain text
- Preserves content

#### Table Features

**Creating Tables:**
1. Click table icon in toolbar
2. Enter rows (1-20)
3. Enter columns (1-10)
4. Click OK
5. Table inserted at cursor

**Editing Tables:**
- Click any cell to edit
- Use Tab to move between cells
- Drag corner to resize table
- Copy/paste works

**Table Styling:**
- Header row (gray background)
- Bordered cells
- Responsive width
- Print-friendly

#### Hyperlink Features

**Insert New Link:**
1. Select text (optional)
2. Click link icon
3. Enter URL
4. Enter link text (if not selected)
5. Link inserted

**Edit Link:**
1. Click inside existing link
2. Click link icon
3. Choose "Edit" (OK)
4. Enter new URL

**Remove Link:**
1. Click inside existing link
2. Click link icon
3. Choose "Remove" (Cancel)
4. Text preserved, link removed

**Link Attributes:**
- Opens in new tab (`target="_blank"`)
- Security enabled (`rel="noopener noreferrer"`)
- Blue styling with underline
- Hover effect

---

## 💾 Save & Load Functionality

### Maker State Management

#### Save Maker State

**What Gets Saved:**
- ✅ All section configurations
- ✅ All standards with content
- ✅ Custom section titles and weights
- ✅ Deployment modality selections
- ✅ Deployment requirements/mitigations
- ✅ SCT name
- ✅ Enable/disable states
- ✅ Section order
- ✅ Timestamp

**How to Save:**
1. Click **"Save Maker State"** button (green)
2. File downloads: `sct-maker-state-YYYY-MM-DDTHH-MM-SS.html`
3. Confirmation toast appears

**File Format:**
- Complete HTML file
- Embedded state in JSON script tag
- Fully functional maker when opened

#### Load Maker State

**How to Load:**
1. Click **"Load Maker State"** button (blue)
2. Select previously saved `.html` file
3. Confirm restoration
4. Maker rebuilds with saved configuration

**Auto-Restore:**
- When opening a saved maker HTML file
- Browser detects embedded state
- Prompts: "Found saved state from [date]. Restore?"
- Click OK to restore, Cancel to ignore

### Generated Tool Data Management

#### Save as HTML

**Button:** "Save as HTML" (yellow/warning)

**What Gets Saved:**
- ✅ Complete assessment tool HTML
- ✅ All entered data (evidence, gaps, actions)
- ✅ All compliance scores
- ✅ Deployment requirements
- ✅ Team information
- ✅ Progress state

**How to Save:**
1. Click **"Save as HTML"** button
2. Tool saves current state to localStorage
3. Downloads complete HTML file
4. Filename: `[sct-name]-tool-YYYY-MM-DD.html`

**Benefits:**
- Standalone file (no server needed)
- Share with team members
- Archive completed assessments
- Version control with timestamps
- Open in any browser

#### Other Export Options

**Export JSON:**
- Raw data in JSON format
- For data processing/analysis
- Import back into tool

**Export to Excel:**
- Formatted spreadsheet
- All sections and scores
- Evidence/gaps/actions included
- Ready for reporting

**Generate PDF:**
- Professional report format
- All assessment data
- Charts and progress indicators
- Print-ready

**Clear Data:**
- Reset tool to default state
- Removes all localStorage data
- Confirmation required
- Page reloads after clearing

---

## 📝 Use Cases & Workflows

### Scenario 1: Building a Custom Tool

```
Day 1: Initial Setup
├─ Open maker (index.html)
├─ Configure sections (Clinical, Logistics, WASH)
├─ Set weights (40%, 40%, 20%)
├─ Select modalities (Embedded, Self-Sustained)
└─ Save maker state → "my-sct-maker-2025-01-15.html"

Day 2: Add Content
├─ Open saved maker file
├─ Restore state (click OK)
├─ Add standards to Clinical section
│  ├─ Patient triage protocols
│  ├─ Infection control measures
│  └─ Medical equipment inventory
├─ Configure deployment requirements
└─ Save maker state → "my-sct-maker-2025-01-16.html"

Day 3: Generate Tool
├─ Open saved maker file
├─ Review all content
├─ Click "Generate Complete HTML Tool"
└─ Save as → "clinical-team-assessment.html"
```

### Scenario 2: Team Assessment

```
Team Leader:
├─ Opens assessment tool
├─ Completes Clinical section
│  ├─ Evidence: "SOPs documented, training completed"
│  ├─ Gaps: "Missing pediatric equipment"
│  ├─ Actions: "Order equipment, schedule training"
│  └─ Score: 2 (In Progress)
├─ Click "Save as HTML"
└─ Sends file to team → "assessment-week1.html"

Team Member:
├─ Opens received file
├─ Sees leader's work (auto-loaded from file)
├─ Completes Logistics section
├─ Click "Save as HTML"
└─ Returns file → "assessment-week1-updated.html"

Final Review:
├─ Opens latest file
├─ Reviews all sections
├─ Generates PDF report
└─ Submits to coordination mechanism
```

### Scenario 3: Multiple Team Profiles

```
Base Configuration:
└─ Create master maker → "base-sct-maker.html"

Clinical Team Tool:
├─ Open base maker
├─ Enable: Clinical, Core, Staffing sections
├─ Disable: Logistics, WASH sections
├─ Generate → "clinical-team-tool.html"

Logistics Team Tool:
├─ Open base maker
├─ Enable: Logistics, WASH, Core sections
├─ Disable: Clinical, Staffing sections
├─ Generate → "logistics-team-tool.html"

Complete Team Tool:
├─ Open base maker
├─ Enable: All sections
├─ Generate → "complete-sct-tool.html"
```

---

## 💡 Tips & Best Practices

### Maker Best Practices

**Organization:**
- ✅ Use descriptive section names
- ✅ Keep standard names concise (title-like)
- ✅ Use consistent formatting across standards
- ✅ Group related standards in same section

**Content Writing:**
- ✅ Be specific and measurable
- ✅ Use bullet points for clarity
- ✅ Include references with hyperlinks
- ✅ Avoid jargon or define terms

**Weights Assignment:**
- ✅ Assign higher weights to critical sections
- ✅ Ensure total equals exactly 100%
- ✅ Document rationale for weight distribution
- ✅ Review weights with stakeholders

**Version Control:**
- ✅ Save maker state frequently
- ✅ Use descriptive filenames with dates
- ✅ Keep backup copies
- ✅ Document major changes in filename
  - Example: `sct-maker-v2-added-wash-2025-01-15.html`

### Assessment Tool Best Practices

**Completing Assessments:**
- ✅ Read standard fully before scoring
- ✅ Provide specific evidence (not "Yes" or "N/A")
- ✅ List concrete gaps, not generic statements
- ✅ Make actions SMART (Specific, Measurable, Achievable, Relevant, Time-bound)

**Data Management:**
- ✅ Save HTML backups regularly
- ✅ Use "Save as HTML" before major changes
- ✅ Name files clearly: `[team]-[date]-[status].html`
- ✅ Keep version history

**Collaboration:**
- ✅ Share HTML files (not screenshots)
- ✅ Document who completed which sections
- ✅ Use consistent scoring criteria across team
- ✅ Review together before final submission

**Reporting:**
- ✅ Export to Excel for data analysis
- ✅ Generate PDF for formal submissions
- ✅ Include timestamp in reports
- ✅ Attach supporting documentation

---

## 🔧 Troubleshooting

### Common Issues

#### "Text lost after hyphen in words like 'pre-deployment'"

**Status:** ✅ FIXED

**Solution:** Updated in latest version. Compound words are now preserved correctly.

---

#### "Table attributes showing as text when inserting"

**Status:** ✅ FIXED

**Solution:** Tables now insert cleanly using DOM manipulation instead of HTML strings.

---

#### "Deployment modality mismatch - selected Self-Sustained but shows Embedded"

**Cause:** Tool loading cached data from localStorage

**Solution:**
1. Open generated tool
2. Click **"Clear Data"** button
3. Confirm clearing
4. Page reloads with fresh data from maker

**Prevention:** Clear data when regenerating tool with different configurations.

---

#### "Lost all my work when closing browser"

**Maker:**
- **Save maker state** before closing
- File persists on disk, not in browser

**Assessment Tool:**
- Auto-saved to localStorage (browser-specific)
- Use **"Save as HTML"** for permanent backups
- localStorage cleared if you:
  - Clear browsing data
  - Use incognito mode
  - Switch browsers

---

#### "Weights don't add up to 100%"

**Check:**
1. Section Management panel
2. View inline weight values
3. Check weight sum alert (bottom of weights section)

**Fix:**
- Adjust weights until sum = 100%
- Alert turns green when valid

---

#### "Can't drag and drop standards"

**Ensure:**
- Grip icon (⋮⋮) is visible
- You're dragging from grip icon, not text
- Standards are in same section (can't drag across sections)

**Browser:**
- Use modern browser (Chrome, Firefox, Edge, Safari)
- Drag & drop requires JavaScript enabled

---

#### "Generated tool doesn't show my changes"

**Maker Changes Not Appearing:**

1. **Verify in Maker:**
   - Expand section
   - Check standard content
   - Confirm it's there

2. **Regenerate Tool:**
   - Click "Generate Complete HTML Tool"
   - Save new file (different name)

3. **Check Console:**
   - Open browser console (F12)
   - Look for debug logs showing captured content

4. **Clear Cache:**
   - In generated tool, click "Clear Data"
   - Reload page

---

### Browser Compatibility

**Fully Supported:**
- ✅ Google Chrome (90+)
- ✅ Mozilla Firefox (88+)
- ✅ Microsoft Edge (90+)
- ✅ Safari (14+)

**Not Supported:**
- ❌ Internet Explorer (any version)
- ❌ Very old browser versions

**Required Features:**
- JavaScript enabled
- LocalStorage enabled
- Drag & Drop API support

---

## 🔍 Technical Details

### Architecture

**Technology Stack:**
- HTML5
- CSS3 (with Bootstrap 5.3)
- Vanilla JavaScript (ES6+)
- FontAwesome 6.4 icons

**Key Libraries:**
- Bootstrap 5.3 - UI components
- FontAwesome 6.4 - Icons
- SheetJS (xlsx) - Excel export

**No Backend Required:**
- Pure client-side application
- No server needed
- No database required
- No installation needed

### Data Storage

**Maker State:**
```json
{
  "toolConfig": { /* Section configurations */ },
  "sectionContent": { /* Editable content */ },
  "deploymentOverrides": { /* Requirements per modality */ },
  "selectedModalities": ["embedded", "self-sustained"],
  "sctName": "Clinical Response Team",
  "timestamp": "2025-01-15T10:30:00.000Z"
}
```

**Assessment Data:**
```json
{
  "teamInfo": { /* Team name, modalities */ },
  "scores": { /* Compliance scores */ },
  "evidence": { /* Evidence descriptions */ },
  "gaps": { /* Identified gaps */ },
  "actions": { /* Action plans */ },
  "deploymentRequirements": { /* Modality requirements */ }
}
```

### File Structure

```
sct-maker/
│
├── index.html              # Main maker file (this is the only file!)
│
└── Generated files:
    ├── sct-maker-state-*.html        # Saved maker configurations
    └── *-tool-*.html                  # Generated assessment tools
```

**Single File Application:**
- Everything in one HTML file
- No external dependencies (uses CDN)
- Completely portable
- Works offline (after initial CDN load)

### Security Considerations

**Data Privacy:**
- All data stored locally (browser localStorage or file downloads)
- No data sent to external servers
- No tracking or analytics
- No cookies used

**Link Security:**
- External links open in new tab
- `rel="noopener noreferrer"` prevents tab-napping
- No JavaScript in href attributes

**Input Sanitization:**
- HTML escaping for user inputs in critical areas
- Content editable with controlled scope
- No eval() or dangerous functions

---

## 📜 License

MIT License - Feel free to use, modify, and distribute.

---

## 🤝 Contributing

Contributions welcome! Areas for improvement:

- [ ] More export formats (Word, CSV)
- [ ] Advanced table features (merge cells, etc.)
- [ ] Image upload and embedding
- [ ] Multi-language support
- [ ] Real-time collaboration
- [ ] Custom themes

---

## 📧 Support

**Author:** Jorge Durand Zurdo
**Email:** joduzu@gmail.com

**Issues:** Found a bug? Have a suggestion?
- Open an issue on GitHub
- Email with detailed description
- Include browser version and steps to reproduce

---

## 🎉 Acknowledgments

Built with ❤️ for emergency medical teams, humanitarian responders, and healthcare professionals worldwide.

Special thanks to:
- WHO for guidance on medical team standards
- Bootstrap team for excellent UI framework
- FontAwesome for comprehensive icon library

---

## 📚 Additional Resources

- [WHO Classification and Minimum Standards for EMTs](https://iris.who.int/server/api/core/bitstreams/f1a9750a-f68b-401c-87ea-c5157a3af6d9/content)
- [Bootstrap Documentation](https://getbootstrap.com/docs/5.3/)
- [FontAwesome Icons](https://fontawesome.com/icons)

---

**Last Updated:** November 2025
**Version:** 2.0
**Status:** Production Ready ✅
