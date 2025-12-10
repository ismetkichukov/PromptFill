# Concept Art Prompt Generator

A **structured prompt generation tool** designed specifically for AI painting (GPT, Nano Banana, etc.). Through a visualized "fill-in-the-blank" interaction method, it helps users quickly build, manage, and iterate complex Prompts.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/Version-0.3.1-orange.svg)
![React](https://img.shields.io/badge/React-18.x-61DAFB.svg)
![Vite](https://img.shields.io/badge/Vite-5.x-646CFF.svg)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38B2AC.svg)

## ✨ Core Features
* **🧩 Intelligent Vocabulary Management**:
* **Category Management**: Supports custom vocabulary categories (e.g., characters, actions, scenes, items), distinguished by colors for clearer visuals.
* **Bidirectional Sync**: When filling in previews on the right, directly add "custom options" which automatically sync back to the left vocabulary without switching back and forth.
* **Category Editor**: Built-in category manager supporting add, delete, and modify operations for categories and their color configurations (12 preset colors).
* **Responsive Layout**: Vocabulary list supports waterfall multi-column layout for more efficient space utilization.
* **📝 Multi-Template System**:
* Supports creating multiple independent Prompt templates (e.g., "Character Concept Breakdown Chart", "3x3 Photography Grid").
* **Independent State**: Variable selections (Selection) for each template do not interfere with each other.
* **Duplicate Cloning**: Supports one-click creation of template duplicates for easy A/B testing or fine-tuning.
* **🖱️ Visual Interaction**:
* **WYSIWYG Editing**: In edit mode, variables are highlighted by category colors, supporting direct text editing and structure adjustments.
* **Drag-and-Drop Insertion**: Directly drag vocabulary cards from the left into the edit area to quickly insert variables.
* **Preview Mode**: Variables in the template (`{{role}}`) are automatically rendered as clickable dropdown menus.
* **Independent Instances**: The same variable appearing multiple times in the template (e.g., `{{color}}`) can have different values selected independently (supports `color-0`, `color-1` independent indexing).
* **💾 Automatic Persistence**:
* Uses LocalStorage to automatically save all changes (templates, vocabulary, category configurations).
* Data is not lost after refreshing the page or closing the browser.
* **🖼️ Image Management**:
* **Preview Image Display**: Each template supports associated preview images, displayed in the template title area for richer visuals.
* **Custom Upload**: Supports uploading custom images to replace default preview images (supports jpg, png, webp formats, etc.).
* **Image Operations**: Hovering over the image shows operation buttons: view large image, upload new image, reset to default image.
* **Large Image Preview**: Clicking the view large image button allows full-screen browsing in Lightbox mode.
* **Decorative Background**: Preview images are displayed as blurred backgrounds at the top of the template, creating an immersive atmosphere.
* **📋 Export and Sharing**:
* **One-Click Copy**: Copy the final generated clean Prompt text.
* **Save as Long Image**: Supports exporting the current filled Prompt template as a high-definition image for easy sharing and archiving.

## 🛠️ Tech Stack
* **Build Tool**: [Vite](https://vitejs.dev/)
* **Frontend Framework**: [React](https://react.dev/)
* **Styling Library**: [Tailwind CSS](https://tailwindcss.com/)
* **Icon Library**: [Lucide React](https://lucide.dev/)
* **Export Tool**: [html2canvas](https://html2canvas.hertzen.com/)
## 🚀 Quick Start
### Prerequisites
Ensure your environment has [Node.js](https://nodejs.org/) installed (recommended v18+).
### Installation and Running
1. **Clone the Project**
```bash
git clone https://github.com/TanShilongMario/PromptFill.git
cd PromptFill
```
2. **Install Dependencies**
```bash
npm install
```
3. **Start Development Server**
```bash
npm run dev
```
The browser will automatically open to `http://localhost:5173`.
4. **Build Production Version**
```bash
npm run build
```
### Quick Start Script
A quick start script is provided in the project root directory. Double-click to launch the service and open the browser with one click:
* **macOS**: `start.command`
* **Windows**: `start.bat`
## 📖 Usage Guide
### Step 1: Manage Categories
* Click the "Manage Categories" button at the top of the left panel.
* Here, you can add new categories, modify existing category names or colors (supports 12 preset colors), and delete unnecessary categories.
* Each category has a unique color identifier to help you quickly identify different types of variables during editing and previewing.
### Step 2: Create Banks
* Click "Create New Variable Group" to add a new variable bank and assign it to a category.
* Add specific options in the bank card:
* **Single Add**: Directly enter the option and press Enter.
* **Bulk Add**: Enter multiple options (one per line), and the system will automatically split and add them.
* Banks support drag-and-drop functionality for quick insertion of variables into the editor.
### Step 3: Edit Templates
* Click the "Edit Template" button in the top-right corner to enter visual editing mode.
* **Drag-and-Drop Insertion**: Hold and drag a bank card from the left into the editor to insert a variable (e.g., `{{weather}}`).
* **Manual Input**: You can also directly type `{{variable_name}}` in the editor, and the system will automatically recognize and render it.
* Variables in the editor will display the corresponding category color for easy identification and management.
* Supports undo/redo functionality for adjusting the template structure at any time.
### Step 4: Preview and Generate
* Switch back to "Preview Interaction" mode.
* Click on a colored variable phrase and select an option from the dropdown menu.
* **Custom Options**: If the option doesn't exist, click "+ Add Custom Option" at the bottom of the dropdown, enter it, and press Enter to use it directly and automatically save it to the bank.
* **Multi-Instance Support**: When the same variable appears multiple times in the template (e.g., `{{color}}`), each instance can independently select different values.
### Step 5: Manage Template Images (Optional)
* **View Preview Image**: If the template is associated with a preview image, it will display in the top-right corner of the template title and serve as a blurred background decoration for the top area.
* **Upload Custom Image**:
1. Hover the mouse over the preview image to reveal three operation buttons.
2. Click the middle "Upload Image" button (image icon).
3. Select a local image file (supports jpg, png, gif, webp, etc.).
4. The image will automatically upload and replace the current preview image.
* **View Full Image**: Click the left "View Full Image" button (zoom icon) to browse image details in full-screen mode.
* **Reset Image**: Click the right "Reset to Default Image" button (undo icon) to restore the template's default preview image.
### Step 6: Export and Share
* **Copy Result**: Click the "Copy Result" button in the top-right corner to copy the final generated clean Prompt text with one click, ready to paste directly into AI drawing tools.
* **Save Long Image**: Click the "Save Long Image" button to export the current filled Prompt template (including the preview image) as a high-definition image (PNG format), convenient for sharing, archiving, or reference.
## 💡 Usage Tips
1. **Bulk Create Banks**: When adding options, you can input multi-line text at once, and the system will automatically split it into multiple options by line.
2. **Template Duplicate Function**: When testing different Prompt effects, use the "Create Duplicate" function to retain the original template for easy comparison.
3. **Color Coding System**: Assign different colors to different types of variables to make complex template structures clearer and easier to read.
4. **Multi-Instance Independent Selection**: When the same variable appears multiple times in the template, the system automatically assigns independent indexes (e.g., `color-0`, `color-1`), allowing different values at each position.
5. **Custom Preview Images**: Upload representative reference images for templates to quickly identify their purposes and make exported long images more visually appealing.
6. **Image Size Recommendations**: Recommended preview image size is around 300x300px square or portrait orientation for optimal display in the interface.
7. **Local Data Safety**: All data (including uploaded images) is stored locally in the browser. Regularly export backups to avoid data loss.
## 📝 Changelog
### Version 0.3.1 (2025-12-09)
* **Startup Optimization**:
* Refactored `start.bat` for compatibility with PowerShell and CMD environments
* Added automatic dependency checks and fixes to resolve missing core dependencies like `vite`
* Optimized browser auto-open logic to ensure it opens automatically upon service startup
* **Engineering Improvements**:
* Added `dev:open` script to `package.json` for unified startup behavior
* Fixed Chinese encoding issues in `start.bat`
* Cleaned up Git tracking for `node_modules`, standardizing project structure
* **Bug Fixes**:
* Resolved Git merge conflicts in `src/data/templates.js`
### Version 0.3.0 (2025-12-08)
* **UI Optimization**:
* Optimized "New Template" button style with unified Premium Button design language for better visual consistency
* Added hover gradient effects and shadow animations to buttons for smoother interaction
* **Feature Documentation**:
* Enhanced documentation for image upload and display features
* Supported custom template preview image uploads
* Image hover operations: view full image, upload new image, reset to default
* Lightbox full-screen image preview mode
* **Documentation Improvements**:
* Restructured usage guide with step-by-step structured explanations
* Added "Usage Tips" section with best practices (including image usage tips)
* Added changelog to record version history
* Supplemented detailed explanations for image management features
### Version 0.2.0
* Added template long image export functionality
* Supported custom category color configuration
* Optimized responsive layout experience
* Fixed multiple known issues
### Version 0.1.0
* Initial version release
* Basic template management functionality
* Bank creation and editing functionality
* Variable fill-in interaction system
## 🤝 Contributing
We welcome Issue submissions or Pull Requests to improve this project!
If you have any suggestions or find a bug, feel free to let us know in [GitHub Issues](https://github.com/TanShilongMario/PromptFill/issues).
## 📄 License

---

**Made with ❤️ by 角落工作室**
