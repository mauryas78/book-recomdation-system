# Personalized Book Recommendation Frontend

This project is a Django-based frontend for a Personalized Book Recommendation API, which delivers tailored book recommendations based on user preferences and reading history. The backend API is built with FastAPI and integrates OpenAI's GPT models for intelligent recommendations.

## Features
- **User Authentication**
  - Login and create user functionality using session keys provided by the backend API.
- **User Preferences Dashboard**
  - Interface for users to update their favorite genres, authors, and other preferences.
- **Book Recommendations**
  - Display of personalized book recommendations fetched from the backend API.
- **Search Functionality**
  - Search books by title, author, or genre.
- **Static UI/UX**
  - Clean and simple design using Django templates and static files.

## Project Structure
```plaintext
project/
├── mysite/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── templates/
│   ├── base.html
│   ├── login.html
│   ├── preferences.html
│   └── recommendations.html
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── api/
│   ├── views.py
│   ├── serializers.py
│   ├── urls.py
│   └── forms.py
└── manage.py
```

## Prerequisites
- Python 3.8+
- Virtual environment (optional but recommended)

## Installation

### Clone the repository:
```bash
git clone <repository-url>
cd <repository-folder>
```

### Create and activate a virtual environment:
```bash
python -m venv myenv
source myenv/bin/activate  # On Windows: myenv\Scripts\activate
```

### Install dependencies:
```bash
pip install django
```

### Start the Django development server:
```bash
python manage.py runserver
```

### Open your browser and navigate to:
[http://127.0.0.1:8000](http://127.0.0.1:8000).

## API Endpoints
The following backend API endpoints are used by the frontend:

### User Authentication:
- `GET /user/create`: Create a new user.
- `GET /user/login`: Login user and retrieve session key.

### Preferences:
- `POST /user/preferences`: Save or update user preferences.

### Recommendations:
- `POST /recommendations`: Fetch personalized book recommendations.

### Search:
- `GET /books/search`: Search books by title, author, or genre.

## Session Management
The frontend uses Django's `request.session` to manage user sessions. Upon successful login, a session key is retrieved from the backend and stored for subsequent API calls.

## Development Plan

1. **Authentication System**
   - Implement login and user creation functionality.

2. **Search Interface**
   - Build the search page to fetch book data.

3. **Preferences Dashboard**
   - Create an interface for updating user preferences.

4. **Recommendations Page**
   - Display personalized book recommendations.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

