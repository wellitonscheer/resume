# Modern Resume Portfolio

A modern, interactive HTML resume showcasing professional experience, projects, and skills with stunning visual effects and animations.

## 🌟 Features

- **Modern Design**: Glass morphism effects with professional navy/slate/gray color palette
- **Interactive Elements**: Hover animations, typing effects, and smooth transitions
- **3D Background**: Animated floating shapes using Three.js
- **Responsive Layout**: Optimized for desktop and mobile devices
- **Professional Icons**: Font Awesome icons throughout for clarity and professionalism
- **Animated Sections**: Project cards with shimmer effects and interactive skill tags

## 🛠️ Technologies Used

- **HTML5**: Semantic markup structure
- **CSS3**: Modern styling with custom properties and animations
- **Tailwind CSS**: Utility-first CSS framework
- **Three.js**: 3D graphics and animations
- **Font Awesome**: Professional icon library
- **Google Fonts**: Inter font family for typography

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for CDN resources)

### Running Locally

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd resume
   ```

2. Open the resume in your browser:
   ```bash
   # Option 1: Direct file opening
   open index.html
   
   # Option 2: Using a local server (recommended)
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

## 📁 Project Structure

```
resume/
├── index.html          # Main resume page
└── README.md          # Project documentation
```

## 🎨 Design Features

### Color Palette
- **Primary**: Navy blue (#1e293b)
- **Secondary**: Slate gray (#475569)
- **Accent**: Light gray (#64748b)
- **Background**: Dark gradient with professional tones

### Visual Effects
- Glass morphism cards with backdrop blur
- Animated 3D floating shapes background
- Typing animation for job title
- Hover effects on interactive elements
- Shimmer animations on project cards

## 📱 Responsive Design

The resume is fully responsive and optimized for:
- Desktop computers (1024px+)
- Tablets (768px - 1023px)
- Mobile devices (320px - 767px)

## 🔧 Customization

### Updating Content
Edit the `index.html` file to update:
- Personal information and contact details
- Work experience and job descriptions
- Projects and their descriptions
- Skills and technologies
- Education background

### Modifying Colors
Update the CSS custom properties in the `<style>` section:
```css
:root {
  --primary-navy: #1e293b;
  --secondary-slate: #475569;
  --accent-gray: #64748b;
  /* Add your custom colors here */
}
```

### Adding New Sections
Follow the existing card structure pattern:
```html
<div class="project-card">
  <div class="flex items-center mb-3">
    <i class="fas fa-icon-name text-3xl mr-3 text-blue-400"></i>
    <div>
      <h3 class="text-xl font-bold text-white">Section Title</h3>
      <p class="text-gray-300">Section Description</p>
    </div>
  </div>
  <!-- Additional content -->
</div>
```

## 🌐 Deployment

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to repository Settings > Pages
3. Select source branch (usually `main`)
4. Your resume will be available at `https://username.github.io/repository-name`

### Netlify
1. Connect your repository to Netlify
2. Set build command: (none needed for static HTML)
3. Set publish directory: `/`
4. Deploy automatically on git push

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to fork this project and customize it for your own use. If you make improvements that could benefit others, pull requests are welcome!

## 📞 Contact

**Welliton Scheer**
- Email: wellitonscheer@gmail.com
- GitHub: [@wellitonscheer](https://github.com/wellitonscheer)
- LinkedIn: [Welliton Scheer](https://linkedin.com/in/wellitonscheer)

---

*Built with ❤️ using modern web technologies*
