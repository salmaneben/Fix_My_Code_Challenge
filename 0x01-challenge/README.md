# Fix My Code Challenge - Part 1 🚀

Welcome to the advanced debugging challenges! This directory contains complex debugging exercises involving web applications, frameworks, and advanced programming concepts across multiple languages and technologies.

## 📁 Project Structure

```
0x01-challenge/
├── square.py              # Python: Square class with geometric methods
├── user.py                # Python: User class with email validation
├── blog/                  # Ruby on Rails: Blog application
├── react-blog/            # JavaScript: React blog application
├── status_server/         # Python: Flask API server
└── README.md             # This file
```

## 🎯 Learning Objectives

Master advanced debugging skills including:
- Web application debugging (Rails, React, Flask)
- Framework-specific error identification
- Complex object-oriented programming issues
- API and server-side debugging
- Frontend and backend integration problems
- Modern web development debugging techniques

## 📝 Challenge Descriptions

### 1. Square Class (Python)
**File**: `square.py`
**Language**: Python 3
**Framework**: Object-Oriented Programming
**Issue**: Geometric calculation class with method implementation errors

**Features to Debug**:
- Rectangle/Square area calculation
- Perimeter calculation methods
- String representation
- Class initialization

**Expected Usage**:
```python
s = Square(width=12, height=9)
print(s)                          # Should show width/height
print(s.area_of_my_square())      # Should calculate area
print(s.permiter_of_my_square())  # Should calculate perimeter
```

### 2. User Class (Python)
**File**: `user.py`
**Language**: Python 3
**Framework**: OOP with Properties
**Issue**: Email validation and property management

**Features to Debug**:
- Email property getter/setter
- Type validation for email
- Error handling for invalid inputs

**Expected Behavior**:
```python
u = User()
u.email = "john@snow.com"
print(u.email)  # Should work correctly
```

### 3. Blog Application (Ruby on Rails)
**Directory**: `blog/`
**Language**: Ruby
**Framework**: Ruby on Rails
**Issue**: Complete Rails application with potential configuration and routing issues

**Application Structure**:
```
blog/
├── Gemfile                    # Ruby dependencies
├── Gemfile.lock              # Locked dependencies
├── config.ru                 # Rack configuration
├── Rakefile                  # Rake tasks
├── app/                      # Application code
│   ├── controllers/          # Rails controllers
│   ├── models/               # Rails models
│   ├── views/                # Rails views
│   └── assets/               # CSS, JS, images
├── config/                   # Rails configuration
├── db/                       # Database files
└── public/                   # Static files
```

**Setup Instructions**:
```bash
cd blog/
gem install bundler
bundle install
rails db:migrate RAILS_ENV=development
rails s -b 0.0.0.0 -p 5000
```

**Admin Credentials**:
- Email: `hbtn@hbtn.io`
- Password: `toto1234`

### 4. React Blog (JavaScript/Node.js)
**Directory**: `react-blog/`
**Language**: JavaScript
**Framework**: React.js + Node.js
**Issue**: Modern web application with frontend/backend integration issues

**Application Features**:
- React frontend with components
- Node.js backend with Express
- Static blog content system
- Responsive design with Bootstrap
- Gulp build system

**Tech Stack**:
- **Frontend**: React.js, Bootstrap, Sass
- **Backend**: Node.js, Express
- **Build Tools**: Gulp, Webpack
- **Styling**: Sass/SCSS

**Setup Instructions**:
```bash
cd react-blog/
npm install -g gulp
npm install
gulp build-all
gulp nodemon
# Navigate to http://localhost:9080/
```

**Available Scripts**:
- `gulp build-all` - Build all assets
- `gulp nodemon` - Start development server
- `gulp watch` - Watch for changes during development

### 5. Status Server (Python/Flask)
**Directory**: `status_server/`
**Language**: Python 3
**Framework**: Flask
**Issue**: REST API server with routing and error handling problems

**API Structure**:
```
status_server/
├── api/
│   ├── __init__.py
│   └── v1/
│       ├── __init__.py
│       ├── app.py          # Main Flask application
│       └── views/          # API endpoints
```

**Features to Debug**:
- Flask application setup
- API routing and blueprints
- Error handling (404, 500)
- JSON response formatting

**Running the Server**:
```bash
cd status_server/
python3 -m api.v1.app
# Server runs on http://0.0.0.0:5000
```

## 🔧 Prerequisites

### Required Software
- **Python 3.x** with pip
- **Ruby** with Rails framework
- **Node.js** with npm
- **Git** for version control

### Development Tools
- **Text Editor/IDE**: VS Code, Vim, or similar
- **Browser**: For testing web applications
- **Terminal/Command Line**: For running commands
- **Database**: SQLite (included with Rails)

## 🚀 Getting Started

1. **Environment Setup**:
   ```bash
   # Python dependencies
   pip3 install flask
   
   # Ruby dependencies
   gem install rails bundler
   
   # Node.js dependencies
   npm install -g gulp-cli
   ```

2. **Clone and Navigate**:
   ```bash
   git clone <repository-url>
   cd Fix_My_Code_Challenge/0x01-challenge
   ```

3. **Choose a Challenge**:
   - Start with simple Python files (`square.py`, `user.py`)
   - Progress to web applications (`blog/`, `react-blog/`, `status_server/`)

## 🔍 Advanced Debugging Techniques

### Python Debugging
- Use `pdb` for interactive debugging
- Add `print()` statements for tracing
- Check error messages and stack traces
- Validate data types and values

### Ruby/Rails Debugging
- Check Rails logs in `log/development.log`
- Use `binding.pry` for interactive debugging
- Verify gem dependencies in `Gemfile`
- Test database migrations

### JavaScript/React Debugging
- Use browser developer tools
- Check console for errors
- Verify Node.js modules installation
- Test API endpoints separately

### Flask Debugging
- Enable debug mode in Flask
- Check request/response formats
- Verify routing configurations
- Test API endpoints with curl or Postman

## 🌐 Web Application Testing

### Blog Application (Rails)
```bash
# Start the server
cd blog/
rails s -b 0.0.0.0 -p 5000

# Test in browser
http://localhost:5000

# Check admin login
Email: hbtn@hbtn.io
Password: toto1234
```

### React Blog
```bash
# Build and start
cd react-blog/
npm install
gulp build-all
gulp nodemon

# Test in browser
http://localhost:9080
```

### Status Server (Flask)
```bash
# Start API server
cd status_server/
python3 -m api.v1.app

# Test API endpoints
curl http://localhost:5000/api/v1/status
```

## 📊 Complexity Levels

| Challenge | Difficulty | Focus Area | Technologies |
|-----------|------------|------------|--------------|
| `square.py` | ⭐⭐ | OOP Basics | Python |
| `user.py` | ⭐⭐ | Properties | Python |
| `status_server/` | ⭐⭐⭐ | API Development | Python, Flask |
| `blog/` | ⭐⭐⭐⭐ | Web Framework | Ruby, Rails |
| `react-blog/` | ⭐⭐⭐⭐⭐ | Modern Web | React, Node.js |

## ✅ Success Criteria

### Python Files
- [ ] Code runs without syntax errors
- [ ] Methods return expected values
- [ ] Proper error handling implemented
- [ ] Code follows Python conventions

### Web Applications
- [ ] Applications start without errors
- [ ] All routes/endpoints respond correctly
- [ ] Frontend displays properly
- [ ] No console errors in browser
- [ ] Database operations work correctly

## 🎓 Skills You'll Develop

- **Backend Development**: Flask, Rails, API design
- **Frontend Development**: React, responsive design
- **Full-Stack Integration**: Frontend-backend communication
- **Build Tools**: Gulp, npm scripts, Rails tasks
- **Database Operations**: Migrations, queries
- **Error Handling**: Proper exception management
- **Testing**: Manual and automated testing techniques

## 📚 Common Issues to Investigate

### Python Applications
- Import errors and module paths
- Incorrect method implementations
- Property decorator issues
- Flask routing problems

### Ruby/Rails Applications
- Gem dependency conflicts
- Database migration issues
- Route configuration errors
- Asset pipeline problems

### JavaScript/React Applications
- npm package installation issues
- Build tool configuration
- Component rendering problems
- API connection issues

## 🔗 Additional Resources

- **Flask Documentation**: https://flask.palletsprojects.com/
- **Rails Guides**: https://guides.rubyonrails.org/
- **React Documentation**: https://reactjs.org/docs/
- **Node.js Documentation**: https://nodejs.org/docs/

## 📈 Progress Tracking

- [ ] `square.py` - Geometric calculations working
- [ ] `user.py` - Email validation functioning
- [ ] `status_server/` - API responding correctly
- [ ] `blog/` - Rails application running
- [ ] `react-blog/` - Full-stack application operational

---

**Advanced Debugging Mastery Awaits! 🎯🚀**

Remember: These challenges simulate real-world debugging scenarios. Take your time to understand each technology stack and debugging approach!
