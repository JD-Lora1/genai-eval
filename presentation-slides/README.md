# Interactive Reveal.js Presentation

This folder contains two versions of the interactive HTML presentation for the **Evaluation Tools and Metrics for Generative AI** workshop:

## 🎯 Available Versions

### **🚀 Recommended: Modern Version (`index_modern.html`)**
- **Completely redesigned UX/UI** with modern design principles
- **Professional visual hierarchy** with cards, gradients, and glassmorphism effects
- **Interactive elements** including progress dots, hover effects, and smooth animations
- **Responsive design** optimized for all devices
- **University branding** with persistent footer and slide counter
- **Enhanced accessibility** with high contrast and semantic markup
- **Font Awesome icons** throughout for visual consistency

### **📄 Classic Version (`index.html`)**
- Original design with basic styling
- Maintained as backup option
- Simpler visual approach

## 🚀 How to Run

### Option 1: Modern Version (Recommended)
1. **Double-click `index_modern.html`** in Windows File Explorer
2. Your default browser will open the presentation
3. **Navigate with arrow keys** or click the navigation arrows
4. **Press `F`** for fullscreen mode
5. **Use progress dots** (top-right) to track your location

### Option 2: Classic Version (Backup)
1. **Double-click `index.html`** in Windows File Explorer
2. Basic presentation functionality

### Option 2: Using a Web Server (for full functionality)
If you encounter any issues with the direct method:

1. **Using Python (if installed):**
   ```bash
   cd presentation-slides
   python -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser

2. **Using Node.js (if installed):**
   ```bash
   cd presentation-slides
   npx serve .
   ```
   Follow the instructions to open in browser

## 🎯 Features (Modern Version)

### **Visual Excellence**
- **Modern AI-inspired color palette** with gradients and glassmorphism effects
- **Professional typography** using Inter and JetBrains Mono fonts
- **Consistent iconography** with Font Awesome 6.4
- **Card-based layout** with hover effects and subtle animations

### **Enhanced Interactivity**
- **Progress indicators** with module tracking dots
- **Smooth animations** for fragment reveals
- **Hover effects** on interactive elements
- **Keyboard shortcuts** (F for fullscreen, arrows for navigation)

### **Professional Features**
- **University branding** with persistent footer
- **Slide counter** showing current position
- **Responsive design** for any screen size
- **Accessibility optimized** with high contrast and semantic markup

## 📖 Navigation Controls

### **Keyboard Shortcuts**
- **Arrow Keys**: Navigate slides
- **Space**: Next slide/fragment
- **Esc**: Overview mode
- **F**: Fullscreen mode (custom shortcut)
- **S**: Speaker notes (if available)
- **?**: Help menu
- **Enter**: Next slide (custom)

### **Visual Indicators**
- **Progress dots** (top-right): Show current module
- **Slide counter** (bottom-right): Current position
- **Footer info** (bottom): University branding and workshop series

## 🎨 Visual Design (Modern Version)

### **Color System**
- **Primary gradient**: Purple-blue for main content (#667eea → #764ba2)
- **Success gradient**: Blue-cyan for positive elements (#4facfe → #00f2fe) 
- **Activity gradient**: Green-cyan for interactive exercises (#43e97b → #38f9d7)
- **Warning/Danger gradients**: For limitations and challenges

### **Typography Hierarchy**
- **Headings**: Inter font family with gradient text effects
- **Body**: Optimized line spacing and contrast
- **Code**: JetBrains Mono for technical content
- **Icons**: Font Awesome 6.4 with contextual colors

### **Layout Components**
- **Cards**: Glassmorphism effect with backdrop blur
- **Grids**: Responsive layouts for different content types
- **Tables**: Modern styling with hover effects
- **Animations**: Subtle slide-in and fade effects

## 📱 Compatibility

- **Modern browsers**: Chrome, Firefox, Safari, Edge
- **Mobile friendly**: Responsive design works on tablets and phones
- **Projection ready**: Optimized for classroom projectors

## 🔗 Fallback Options

If you can't run the modern HTML presentation:
1. **Classic version**: Use `index.html` for basic functionality
2. **Markdown version**: Use `../presentation.md` for text content
3. **PDF export**: Print from browser maintaining visual design
4. **PowerPoint**: Convert using online converters if needed

## 📚 Additional Resources

- **`DESIGN_IMPROVEMENTS.md`**: Detailed documentation of UX improvements
- **Design system**: Custom CSS properties for easy customization
- **Font loading**: Optimized with preconnect for better performance

---

## 🌟 Quick Start

**For the best experience:** Open `index_modern.html` and enjoy the professional, interactive presentation!

**Need something simpler?** Use `index.html` as a fallback.

*Ready to present? The modern version will make your workshop look amazing! 🚀*
