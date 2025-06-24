# Chatbot UI

A modern, responsive chatbot interface designed specifically for nutrition products. This eco-friendly chat interface provides customers with an intuitive way to learn about nutritional powders.

## 🌱 Features

- **Plant-based Design Theme**: Earth-tone color palette reflecting BhavaEarth's sustainable brand
- **Responsive Layout**: Optimized for both desktop and mobile devices
- **Quick Action Buttons**: Pre-defined questions for common inquiries
- **Real-time Typing Indicators**: Shows when the bot is processing responses
- **Smooth Animations**: Professional fade-in effects and hover interactions
- **Django Integration Ready**: Built with Django backend integration in mind

## 🎨 Design Highlights

- **Brand Colors**: 
  - Primary Green: `#2d5016`
  - Light Green: `#8bc34a`
  - Cream Background: `#f8f5f0`
  - Earth Brown: `#6d4c41`
- **Plant-themed Icons**: Seedling, leaf, and nature-inspired elements
- **Modern Chat Interface**: WhatsApp-style message bubbles
- **Accessibility**: Proper contrast ratios and semantic markup

## 🚀 Quick Start

### Prerequisites

- Django 3.2+ (for backend integration)
- Modern web browser with JavaScript enabled
- Bootstrap 5.3.2 (loaded via CDN)
- Font Awesome 6.4.0 (loaded via CDN)

### Installation

1. **Clone or download** the HTML file to your Django project
2. **Place the HTML file** in your Django templates directory
3. **Update your Django URLs** to serve the chatbot page

```python
# urls.py
from django.urls import path
from .views import *

urlpatterns = [
    path('',index, name='index'),
]
```

4. **Create Django views** to handle the chatbot

```python
# views.py
from django.shortcuts import render

def chatbot_view(request):
    return render(request, 'index.html')

```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in your Django project root:

```env
# Django Settings
DEBUG=True
SECRET_KEY=your-secret-key-here
```

### Django Settings

Add to your `settings.py`:

```python
# settings.py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'llmapp',  # Your chatbot app
]

# Static files configuration
STATIC_URL = '/static/'
STATICFILES_DIRS = [
    BASE_DIR / "static",
]
```

## 🔒 Security Features

- **CSRF Protection**: Built-in Django CSRF token support
- **Input Sanitization**: User messages are properly escaped
- **Rate Limiting**: Can be easily integrated with Django rate limiting
- **Session Management**: Supports Django's session framework

## 🧪 Testing

### Manual Testing Checklist

- [ ] Send message functionality works
- [ ] Quick action buttons trigger correctly
- [ ] Typing indicator appears and disappears
- [ ] Messages scroll properly
- [ ] Mobile responsive design works
- [ ] All animations function smoothly
- [ ] CSRF token is properly included in requests


## 🚀 Deployment

### Production Checklist

- [ ] Set `DEBUG = False` in Django settings
- [ ] Configure proper database (PostgreSQL recommended)
- [ ] Set up static file serving
- [ ] Configure HTTPS
- [ ] Set up proper logging
- [ ] Configure rate limiting
- [ ] Set up monitoring

### Environment Setup

```bash
# Install dependencies
pip install django gunicorn psycopg2-binary

# Collect static files
python manage.py collectstatic

# Run migrations
python manage.py migrate

# Start production server
gunicorn myproject.wsgi:application
```


## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


## 📈 Roadmap

- [ ] Voice message support
- [ ] File upload capability
- [ ] Multi-language support
- [ ] AI-powered product recommendations
- [ ] Integration with order management system
- [ ] Customer support ticket creation
- [ ] Real-time chat with human agents

---
