# Harbor - AI-Powered Tab Manager for Efficient Browser Organization

Harbor is a browser extension that helps users efficiently organize and manage their tabs using AI-powered grouping and a Kanban-style interface. The extension automatically categorizes tabs, removes duplicates, and provides seamless integration with third-party services like Notion and Raindrop.

Harbor addresses the common problem of tab overload by providing intelligent tab management features. The extension uses AI to automatically group related tabs, allows users to create collections for better organization, and supports both automatic and manual tab management workflows. With features like automatic duplicate removal, customizable backup options, and multi-language support (English, Spanish, and Chinese), Harbor helps users maintain a clean and productive browsing environment.

## Repository Structure
```
.
├── _locales/                 # Localization files for multiple languages
│   ├── en/                  # English translations
│   ├── es/                  # Spanish translations
│   └── zh_CN/              # Chinese translations
├── _metadata/               # Extension metadata and verification files
├── manifest.json           # Chrome extension manifest configuration
├── popup.html             # Extension popup interface
├── static/                # Static assets and background scripts
│   └── background/        # Background service worker scripts
└── tabs/                  # Tab management interface files
    ├── harbor.html       # Main Harbor interface
    └── welcome.html      # Welcome/onboarding page
```

## Usage Instructions
### Prerequisites
- Google Chrome browser (latest version recommended)
- Sufficient permissions for tab management and storage access
- Active internet connection for AI-powered features

### Installation
1. **Chrome Web Store Installation**
```bash
# Visit the Chrome Web Store and search for "Harbor - AI-Powered Tab Manager"
# Click "Add to Chrome" to install the extension
```

2. **Developer Installation**
```bash
# Clone the repository
git clone [repository-url]

# Load unpacked extension in Chrome
1. Open Chrome and navigate to chrome://extensions/
2. Enable "Developer mode"
3. Click "Load unpacked" and select the repository folder
```

### Quick Start
1. Click the Harbor icon in your browser toolbar to open the popup interface
2. Use Alt+H (or Option+H on Mac) to open the main Harbor interface
3. Drag and drop tabs into collections for organization
4. Use Alt+G (or Option+G on Mac) to trigger AI-powered tab grouping

### More Detailed Examples
1. **Creating Tab Collections**
```javascript
// Right-click on any tab and select "Send to Harbor"
// Or use Alt+Q (Option+Q on Mac) to send all tabs to Harbor
```

2. **AI-Powered Tab Grouping**
```javascript
// Select tabs you want to group
// Click "Group by AI" or use Alt+G shortcut
// Harbor will automatically categorize tabs based on content
```

3. **Integration with Third-Party Services**
```javascript
// Navigate to Settings > Integrations
// Connect with Notion or Raindrop
// Use "Sync to [Service]" option in tab context menu
```

### Troubleshooting
1. **AI Grouping Not Working**
- Verify internet connection
- Check remaining AI grouping usage in free tier
- Ensure proper permissions are granted

2. **Auto-Backup Issues**
- Check file access permissions
- Verify backup file path is correct
- Ensure sufficient storage space

3. **Performance Optimization**
- Enable "Auto Remove Duplicates" in settings
- Use collections to organize tabs
- Regularly clean up unused collections

## Data Flow
Harbor processes tab data through a pipeline of collection, organization, and synchronization steps. The extension manages tab metadata locally while leveraging cloud services for AI-powered features and third-party integrations.

```ascii
[Browser Tabs] -> [Harbor Extension] -> [Local Storage]
                        |                     |
                        v                     v
                [AI Grouping API] <- [Tab Collections]
                        |                     |
                        v                     v
                [Third-Party Services] <- [Backup Files]
```

Key Component Interactions:
1. Background service worker monitors tab creation and updates
2. Popup interface provides quick access to common actions
3. Main Harbor interface manages collections and groups
4. AI service processes tab content for intelligent grouping
5. Local storage maintains user preferences and collection data
6. Backup system periodically saves collections to local files
7. Integration layer syncs data with third-party services