
# Login with Google and Facebook

### This Django project provides authentication via Google and Facebook APIs. 

### You can try it with [Deployment link](https://vicplace.pythonanywhere.com/) 🐍

## Prerequisites

Before setting up and using this project, ensure you have the following prerequisites:

1. **Python**: Install Python from the [official Python website](https://www.python.org/downloads/).

2. **Git**: If you're using Git, you can download it from the [official Git website](https://git-scm.com/downloads).

3. **Google Cloud Developers Console**: Create an account and set up an app on the [Google Cloud Developers Console](https://console.cloud.google.com/). Here, you can generate API keys, IDs, and set URLs for Google authentication.

4. **Facebook for Developers**: Create an account and set up an app on [Meta Connect](https://developers.facebook.com/). Here, you can generate API keys, IDs, and set URLs for Facebook authentication.

## Installation

1. **Clone the Repository**: In your terminal, use the following command to clone this repository:

   ```bash
   git clone https://github.com/vicnesterenko/Login-with-Google-and-Facebook
   ```

2. **Create a Virtual Environment**:

   **On Windows:**

   ```bash
   cd path\to\your\project\directory
   python -m venv your_venv_name
   your_venv_name\Scripts\activate
   ```

   **On macOS and Linux:**

   ```bash
   cd path/to/your/project/directory
   python3 -m venv your_venv_name
   source your_venv_name/bin/activate
   ```

3. **Install Dependencies**: Install the required dependencies using pip:

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply Database Migrations**:

   Run the following commands to apply database migrations:

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

## Usage

1. **Create an Admin Account**:

   ```bash
   python manage.py createsuperuser
   ```
   
2. **Configure API Keys and IDs**:

   Replace `API_KEY` and `ID` values for each app in the admin page located at `http://127.0.0.1:8000/admin/socialaccount/socialapp/`.

3. **Start the Django Development Server**:

   ```bash
   python manage.py runserver
   ```
   Your application will be accessible at `http://127.0.0.1:8000/`.

## Notes

For Facebook authentification we need a secure connection(https). To run the server locally or on the deployment platform try this:
1. **Install libs**:

   ```bash
   pip install Werkzeug
   pip install django-extensions
   pip install pyOpenSSL
   ```
2. **Run server with this command**:

   ```bash
   python manage.py runserver_plus --key-file selftest-key --cert-file selftest-cert localhost:800
   ```

   ### About problems with Facebook authentification

   Facebook brings some problems with domains when I deploy it in [Pythonenywhere platform](https://www.pythonanywhere.com/). In local usage, it makes authentification for Facebook.

