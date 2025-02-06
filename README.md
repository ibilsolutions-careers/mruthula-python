# Django Book Management App

A simple book management system built with Django and MongoDB.

## Features

- View list of all books
- Add new books
- Edit existing books
- Delete books
- Basic responsive design

## Prerequisites

- Python 3.8 or higher
- MongoDB (installed locally)
- pip (Python package manager)

## Setup Instructions

1. **Clone the repository**
```bash
git clone <your-repository-url>
cd book-management
```

2. **Create and activate virtual environment**
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python -m venv venv
source venv/bin/activate
```

3. **Install required packages**
```bash
pip install -r requirements.txt
```

4. **Configure MongoDB**
- Make sure MongoDB is running on your system
- The database will be created automatically when you run migrations

5. **Apply migrations**
```bash
python manage.py makemigrations
python manage.py migrate
```

6. **Run the development server**
```bash
python manage.py runserver
```

7. **Access the application**
- Open your browser and go to `http://localhost:8000`

## Project Structure
```
book_management/
├── books/                    # Main app directory
│   ├── models.py            # Book model
│   ├── views.py             # View functions
│   ├── urls.py              # URL configurations
│   └── templates/           # HTML templates
│       └── books/
│           ├── list.html    # Book list page
│           └── form.html    # Add/Edit form
├── static/                  # Static files
│   └── css/
│       └── style.css       # Main stylesheet
├── manage.py               # Django management script
└── requirements.txt        # Project dependencies
```

## Book Model Fields

- `title` (CharField): Book title
- `author` (CharField): Author name
- `published_year` (IntegerField): Year of publication

## Available URLs

- Home/Book List: `/`
- Add New Book: `/add/`
- Edit Book: `/edit/<id>/`
- Delete Book: `/delete/<id>/`

## Basic Usage

1. **View Books**
   - Navigate to the home page to see all books
   - Books are displayed in a simple table format

2. **Add a Book**
   - Click "Add New Book" button
   - Fill in the required fields
   - Click "Save" to add the book

3. **Edit a Book**
   - Click "Edit" next to any book
   - Modify the fields
   - Click "Save" to update

4. **Delete a Book**
   - Click "Delete" next to any book
   - Confirm deletion when prompted
