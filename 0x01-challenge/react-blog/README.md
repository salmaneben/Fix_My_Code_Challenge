# React Blog Application ⚛️

A modern full-stack blog application built with React.js frontend and Node.js backend. This application demonstrates modern web development practices and may contain bugs that need to be identified and fixed as part of the debugging challenge.

## 🏗️ Application Architecture

### Tech Stack
- **Frontend**: React.js, Bootstrap, Sass
- **Backend**: Node.js, Express.js
- **Build Tools**: Gulp, Webpack, Babel
- **Styling**: Sass/SCSS, Bootstrap
- **Progress Indicator**: NProgress library

### Directory Structure
```
react-blog/
├── package.json              # Node.js dependencies and scripts
├── gulpfile.js              # Gulp build configuration
├── config.js                # Application configuration
├── app.js                   # Main Node.js server file
├── README.md                # This file
├── bin/
│   └── www.js              # Server startup script
├── controllers/             # Express.js controllers
│   └── post.controller.js  # Post handling logic
├── routes/                 # Express.js routes
│   └── post.routes.js      # Post API routes
├── views/                  # View templates
│   ├── index.jade          # Main template
│   └── error/              # Error pages
│       └── 500.html
├── src/                    # React source code
│   ├── client.js           # React client entry point
│   ├── routes.jsx          # React Router configuration
│   ├── alt.js              # Flux implementation
│   ├── analytics.js        # Analytics integration
│   ├── IncludeHandler.js   # Content inclusion handler
│   ├── actions/            # Flux actions
│   ├── components/         # React components
│   ├── mixins/             # React mixins
│   └── stores/             # Flux stores
├── sass/                   # Sass stylesheets
│   ├── common.scss         # Common styles
│   ├── font.scss           # Font definitions
│   ├── footer.scss         # Footer styles
│   ├── full-post.scss      # Full post view styles
│   ├── pagination.scss     # Pagination styles
│   └── post-list.scss      # Post list styles
├── public/                 # Static files and compiled assets
│   ├── css/                # Compiled CSS
│   ├── scripts/            # Compiled JavaScript
│   ├── images/             # Image assets
│   ├── fonts/              # Font files
│   ├── lib/                # Third-party libraries
│   │   └── nprogress/      # Progress bar library
│   └── static/             # Static content
│       └── md/             # Markdown content
└── react-bootstrap-0.26.4/ # React Bootstrap components
    ├── src/                # Bootstrap React components
    ├── docs/               # Documentation
    ├── test/               # Test files
    └── tools/              # Build tools
```

## 🚀 Setup Instructions

### Prerequisites
- **Node.js** (version 12+ recommended)
- **npm** (comes with Node.js)
- **Gulp CLI** (global installation)

### Installation Steps

1. **Install Gulp globally**:
   ```bash
   npm install -g gulp-cli
   ```

2. **Install project dependencies**:
   ```bash
   cd react-blog/
   npm install
   ```

3. **Build the application**:
   ```bash
   gulp build-all
   ```

## 🏃‍♂️ Running the Application

### Development Mode
```bash
# Start the development server with auto-restart
gulp nodemon

# Application will be available at:
# http://localhost:9080
```

### Production Mode
```bash
# Build all assets
gulp build-all

# Start the server
node app.js
```

### Development with Auto-reload
```bash
# In one terminal: build and watch for changes
gulp watch

# In another terminal: start the server
gulp nodemon
```

## 📜 Available Scripts

### Gulp Tasks
```bash
# Build all assets (CSS, JS, etc.)
gulp build-all

# Start development server with auto-restart
gulp nodemon

# Watch for file changes and rebuild
gulp watch

# Build CSS from Sass
gulp build-css

# Build JavaScript with Webpack
gulp build-js

# Copy static assets
gulp copy-assets
```

### npm Scripts
```bash
# Install dependencies
npm install

# Start the application
npm start

# Run tests (if configured)
npm test
```

## 🔧 Configuration

### Application Configuration (`config.js`)
```javascript
module.exports = {
    baseUrl: 'http://localhost:9080',
    itemsPerPage: 5,
    port: 9080,
    // ... other configuration options
};
```

### Server Configuration (`app.js`)
Main Express.js server configuration:
- Route definitions
- Middleware setup
- Static file serving
- Error handling

### Build Configuration (`gulpfile.js`)
Gulp build pipeline configuration:
- Sass compilation
- JavaScript bundling with Webpack
- Asset copying and optimization
- Development server setup

## ⚛️ React Architecture

### Components Structure
```
src/components/
├── App.jsx              # Main application component
├── Header.jsx           # Navigation header
├── Footer.jsx           # Site footer
├── PostList.jsx         # Blog post listing
├── PostDetail.jsx       # Individual post view
├── Pagination.jsx       # Page navigation
└── LoadingIndicator.jsx # Loading states
```

### Flux Architecture
- **Actions**: User interactions and API calls
- **Stores**: Application state management
- **Components**: View layer with React

### Routing (`src/routes.jsx`)
React Router configuration for:
- Homepage with post list
- Individual post pages
- Pagination routes
- Error pages

## 🎨 Styling Architecture

### Sass Structure
```
sass/
├── common.scss         # Base styles and resets
├── font.scss          # Font definitions and imports
├── footer.scss        # Footer component styles
├── full-post.scss     # Individual post page styles
├── pagination.scss    # Pagination component styles
└── post-list.scss     # Post listing styles
```

### Bootstrap Integration
- React Bootstrap components
- Custom Bootstrap theme
- Responsive grid system
- Component-based styling

### Build Process
1. Sass files compiled to CSS
2. CSS minified and autoprefixed
3. Assets fingerprinted for caching
4. Source maps generated for debugging

## 🔌 API Endpoints

### Post Controller (`controllers/post.controller.js`)
```javascript
// Get all posts with pagination
GET /posts/:pageNum?

// Load posts via AJAX
GET /api/posts

// Get individual post
GET /post/:slug
```

### Static Content
- Blog posts stored as JSON (`public/static/posts.json`)
- Markdown content in `public/static/md/`
- Images and assets in `public/` directories

## 🐛 Common Issues to Debug

### Build Issues
- [ ] Gulp tasks failing to compile
- [ ] Webpack configuration errors
- [ ] Sass compilation problems
- [ ] Missing dependencies

### React Issues
- [ ] Component rendering errors
- [ ] Router configuration problems
- [ ] State management issues
- [ ] Props passing errors

### Express Server Issues
- [ ] Route configuration errors
- [ ] Middleware setup problems
- [ ] Static file serving issues
- [ ] API endpoint errors

### Asset Loading Issues
- [ ] CSS not loading properly
- [ ] JavaScript bundle errors
- [ ] Image path problems
- [ ] Font loading issues

### Browser Console Errors
- [ ] JavaScript runtime errors
- [ ] React component warnings
- [ ] Network request failures
- [ ] CORS issues

## 🧪 Testing and Debugging

### Browser Developer Tools
```bash
# Open browser console to check for:
# - JavaScript errors
# - Network requests
# - React component tree
# - Performance issues
```

### Server Debugging
```bash
# Check server logs
node app.js

# Use nodemon for auto-restart during development
gulp nodemon

# Check specific routes
curl http://localhost:9080/api/posts
```

### Build Debugging
```bash
# Check Gulp task output
gulp build-all --verbose

# Test individual build steps
gulp build-css
gulp build-js
```

## 📊 Performance Monitoring

### NProgress Integration
- Progress bar for navigation
- AJAX request indicators
- Page loading feedback

### Optimization Features
- Asset minification
- File fingerprinting
- Gzip compression
- Image optimization

## 🔍 Debugging Checklist

### Application Won't Start
- [ ] Check Node.js version compatibility
- [ ] Verify all npm packages installed
- [ ] Check port availability (default: 9080)
- [ ] Review package.json scripts
- [ ] Check for syntax errors in main files

### Build Failures
- [ ] Run `npm install` to ensure dependencies
- [ ] Check Gulp installation (`gulp --version`)
- [ ] Verify gulpfile.js syntax
- [ ] Check Sass file syntax
- [ ] Review webpack configuration

### Page Not Loading
- [ ] Check Express routes configuration
- [ ] Verify React Router setup
- [ ] Check for JavaScript console errors
- [ ] Verify static asset paths

### Styling Issues
- [ ] Check Sass compilation
- [ ] Verify CSS file generation
- [ ] Check Bootstrap integration
- [ ] Review responsive design breakpoints

## 📚 Dependencies

### Main Dependencies
```json
{
  "express": "Server framework",
  "react": "Frontend library",
  "react-dom": "React DOM rendering",
  "react-router": "Client-side routing",
  "alt": "Flux implementation",
  "superagent": "HTTP requests",
  "jade": "Template engine"
}
```

### Build Dependencies
```json
{
  "gulp": "Build system",
  "webpack": "Module bundler",
  "babel": "JavaScript compiler",
  "sass": "CSS preprocessor",
  "nodemon": "Development server"
}
```

## 🎯 Success Criteria

The React blog application should:
- [ ] Start without errors on `gulp nodemon`
- [ ] Display homepage at http://localhost:9080
- [ ] Load and display blog posts correctly
- [ ] Navigate between pages smoothly
- [ ] Show proper styling with Bootstrap
- [ ] Handle AJAX requests correctly
- [ ] Display loading indicators
- [ ] Work responsively on different screen sizes

## 📈 Learning Outcomes

After fixing this application, you should understand:
- Modern React.js development patterns
- Node.js and Express.js server setup
- Gulp build system configuration
- Sass/SCSS preprocessing
- Webpack module bundling
- Client-side routing with React Router
- Flux architecture for state management
- Full-stack JavaScript development

## 🔗 Technology Resources

- **React Documentation**: https://reactjs.org/docs/
- **Express.js Guide**: https://expressjs.com/
- **Gulp Documentation**: https://gulpjs.com/
- **Sass Documentation**: https://sass-lang.com/
- **Bootstrap Documentation**: https://getbootstrap.com/

---

**Happy React Debugging! ⚛️🚀**

Remember to check both browser console and server logs for comprehensive debugging information!
