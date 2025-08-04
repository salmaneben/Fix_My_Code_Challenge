# Rails Blog Application 📝

A Ruby on Rails blog application with user authentication, post management, and admin functionality. This application may contain bugs that need to be identified and fixed as part of the debugging challenge.

## 🏗️ Application Architecture

### Tech Stack
- **Framework**: Ruby on Rails
- **Database**: SQLite (development)
- **Authentication**: Built-in Rails authentication
- **Styling**: Custom CSS with normalize.css
- **Asset Pipeline**: Rails asset management

### Directory Structure
```
blog/
├── Gemfile                 # Ruby dependencies
├── Gemfile.lock           # Locked dependency versions
├── config.ru              # Rack configuration
├── Rakefile               # Rake tasks
├── README.md              # This file
├── app/                   # Main application code
│   ├── assets/            # CSS, JS, images
│   │   ├── images/
│   │   ├── javascripts/
│   │   └── stylesheets/
│   │       ├── _normalize.scss
│   │       └── application.css
│   ├── channels/          # Action Cable channels
│   ├── controllers/       # Rails controllers
│   │   └── application_controller.rb
│   ├── helpers/           # View helpers
│   │   ├── application_helper.rb
│   │   └── posts_helper.rb
│   ├── jobs/              # Background jobs
│   ├── mailers/           # Email handling
│   ├── models/            # Data models
│   └── views/             # View templates
├── bin/                   # Executable scripts
│   ├── bundle
│   ├── rails
│   ├── rake
│   ├── setup
│   ├── spring
│   └── update
├── config/                # Configuration files
│   ├── application.rb     # Main app configuration
│   ├── boot.rb           # Boot sequence
│   ├── database.yml      # Database configuration
│   ├── environment.rb    # Environment setup
│   ├── puma.rb          # Puma server config
│   ├── routes.rb        # Route definitions
│   ├── secrets.yml      # Secret keys
│   ├── spring.rb        # Spring configuration
│   ├── environments/    # Environment-specific configs
│   ├── initializers/    # Initialization scripts
│   └── locales/         # Internationalization
├── db/                   # Database files
│   ├── development.sqlite3  # SQLite database
│   ├── schema.rb           # Database schema
│   ├── seeds.rb           # Seed data
│   └── migrate/           # Database migrations
├── lib/                  # Library code
│   ├── assets/
│   └── tasks/           # Rake tasks
├── log/                 # Log files
│   └── development.log  # Development logs
├── public/              # Static files
│   ├── 404.html         # Error pages
│   ├── 422.html
│   ├── 500.html
│   ├── favicon.ico
│   └── robots.txt
├── test/                # Test files
│   ├── controllers/
│   ├── fixtures/
│   ├── helpers/
│   ├── integration/
│   ├── mailers/
│   ├── models/
│   └── test_helper.rb
├── tmp/                 # Temporary files
│   ├── cache/
│   ├── pids/
│   └── restart.txt
└── vendor/              # Third-party code
    └── assets/
```

## 🚀 Setup Instructions

### Prerequisites
- **Ruby** (version 2.7+ recommended)
- **Rails** (version 5.x or 6.x)
- **Bundler** gem
- **SQLite3** (for development database)

### Installation Steps

1. **Install Bundler** (if not already installed):
   ```bash
   gem install bundler
   ```

2. **Install Dependencies**:
   ```bash
   cd blog/
   bundle install
   ```

3. **Setup Database**:
   ```bash
   rails db:migrate RAILS_ENV=development
   ```

4. **Seed Database** (optional):
   ```bash
   rails db:seed
   ```

## 🏃‍♂️ Running the Application

### Development Server
```bash
# Start the Rails server
rails s -b 0.0.0.0 -p 5000

# Alternative: Specify environment
rails server -e development -p 5000
```

### Access the Application
- **URL**: http://localhost:5000
- **Admin Interface**: Available after login

### Rails Console
For debugging and testing:
```bash
rails console
# or
rails c
```

## 👨‍💼 Admin Access

### Default Admin Account
- **Email**: `hbtn@hbtn.io`
- **Password**: `toto1234`

### Admin Features
- Create, edit, and delete blog posts
- Manage user accounts
- View application statistics
- Access administrative dashboard

## 🔧 Configuration Files

### Database Configuration (`config/database.yml`)
```yaml
development:
  adapter: sqlite3
  database: db/development.sqlite3
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  timeout: 5000
```

### Routes Configuration (`config/routes.rb`)
Defines URL routing for the application:
```ruby
Rails.application.routes.draw do
  # Add your routes here
  root 'posts#index'
  resources :posts
  # ... other routes
end
```

### Application Configuration (`config/application.rb`)
Main application settings and middleware configuration.

## 🎨 Styling and Assets

### CSS Framework
- **Normalize.css**: Cross-browser CSS normalization
- **Custom Styles**: Application-specific styling
- **Responsive Design**: Mobile-friendly layouts

### Asset Pipeline
Rails asset pipeline for:
- CSS compilation and minification
- JavaScript bundling
- Image optimization
- File fingerprinting for caching

## 🐛 Common Issues to Debug

### Database Issues
- [ ] Migration errors
- [ ] Missing database tables
- [ ] Seed data problems
- [ ] Database connection issues

### Authentication Issues
- [ ] User login/logout functionality
- [ ] Password validation
- [ ] Session management
- [ ] Admin access controls

### Routing Issues
- [ ] Incorrect route definitions
- [ ] Missing controller actions
- [ ] Route parameter problems
- [ ] Redirect loops

### View Issues
- [ ] Template rendering errors
- [ ] Missing view files
- [ ] Helper method issues
- [ ] Asset loading problems

### Model Issues
- [ ] Validation errors
- [ ] Association problems
- [ ] Callback issues
- [ ] Database query errors

## 🧪 Testing

### Run Tests
```bash
# Run all tests
rails test

# Run specific test files
rails test test/controllers/
rails test test/models/

# Run with verbose output
rails test -v
```

### Test Structure
- **Unit Tests**: Model testing
- **Functional Tests**: Controller testing
- **Integration Tests**: Full application flow testing

## 📊 Debugging Tools

### Rails Console
```bash
rails console
# Interactive Ruby environment with app loaded
```

### Rails Logs
```bash
# View development logs
tail -f log/development.log

# View in real-time with colors
tail -f log/development.log | grep -E "(ERROR|WARN|INFO)"
```

### Rails Routes
```bash
# Display all routes
rails routes

# Search for specific routes
rails routes | grep posts
```

### Database Console
```bash
# Access database directly
rails dbconsole
# or
rails db
```

## 🔍 Debugging Checklist

### Application Won't Start
- [ ] Check Ruby version compatibility
- [ ] Verify all gems are installed (`bundle install`)
- [ ] Check database configuration
- [ ] Review application logs
- [ ] Verify server port availability

### Database Issues
- [ ] Run migrations (`rails db:migrate`)
- [ ] Check database file permissions
- [ ] Verify SQLite3 installation
- [ ] Review migration files for errors

### Page Not Loading
- [ ] Check routes configuration
- [ ] Verify controller exists and has correct action
- [ ] Ensure view template exists
- [ ] Check for syntax errors in views

### Authentication Not Working
- [ ] Verify user model and authentication logic
- [ ] Check session configuration
- [ ] Review login/logout routes
- [ ] Test with admin credentials

## 📚 Rails Resources

### Documentation
- **Rails Guides**: https://guides.rubyonrails.org/
- **Rails API**: https://api.rubyonrails.org/
- **Ruby Documentation**: https://ruby-doc.org/

### Debugging Tools
- **Pry**: Interactive debugger (`gem 'pry-rails'`)
- **Byebug**: Ruby debugger
- **Rails Panel**: Chrome extension for Rails debugging

## 🎯 Success Criteria

The blog application should:
- [ ] Start without errors on `rails server`
- [ ] Display homepage at http://localhost:5000
- [ ] Allow admin login with provided credentials
- [ ] Support basic CRUD operations for posts
- [ ] Handle authentication correctly
- [ ] Display proper error pages for 404/500 errors
- [ ] Load all assets (CSS, JS) without errors

## 📈 Learning Outcomes

After fixing this application, you should understand:
- Rails application structure and conventions
- MVC (Model-View-Controller) architecture
- Rails routing and RESTful design
- Database migrations and Active Record
- Rails asset pipeline
- Authentication and authorization in Rails
- Debugging techniques for Rails applications

---

**Happy Rails Debugging! 🚂💎**

Remember to check the Rails logs (`log/development.log`) for detailed error information when debugging issues!
