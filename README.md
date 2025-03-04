# Django Project Setup Guide for macOS

This guide will walk you through the process of setting up a Django project on macOS.

## Prerequisites

- macOS system
- Homebrew (package manager for macOS)
- Python 3.x (Recommended version)

---

## Step 1: Install Homebrew (If Not Installed)

Homebrew is a package manager for macOS that makes it easy to install dependencies.

Run the following command to install Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Verify installation:

```bash
brew --version
```

---

## Step 2: Install Python

macOS comes with Python pre-installed, but it’s recommended to install the latest version.

```bash
brew install python
```

Check the Python version:

```bash
python3 --version
```

---

## Step 3: Install Virtual Environment

Create a virtual environment to manage project dependencies. It is a best practice to isolate dependencies for each project.

```bash
python3 -m venv myenv
```

Activate the virtual environment:

```bash
source myenv/bin/activate
```

---

## Step 4: Install Django

With the virtual environment activated, install Django using `pip`.

```bash
pip install django
```

Verify installation:

```bash
django-admin --version
```

---

## Step 5: Create a Django Project

Run the following command to create a new Django project:

```bash
django-admin startproject myproject
cd myproject
```

---

## Step 6: Run the Development Server

To ensure everything is set up correctly, start the Django development server:

```bash
python manage.py runserver
```

Open your browser and visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) to see the default Django welcome page.

---

## Step 7: Create a Django App

Inside the project directory, create an app by running the following:

```bash
python manage.py startapp myapp
```

Now, open `myproject/settings.py` and add `'myapp'` to the `INSTALLED_APPS` list.

---

## Step 8: Apply Migrations

To set up the database, run the migrations:

```bash
python manage.py migrate
```

---

## Step 9: Create a Superuser (Admin)

To access the Django admin panel, you need to create a superuser:

```bash
python manage.py createsuperuser
```

Follow the prompts to set up the admin username, email, and password.

Access the admin panel at [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/).

---

## Step 10: Start Building!

Congratulations! You've set up your Django project. You can now begin building your application!

---

## Deleting the Project

If you want to delete the project, follow these steps:

### Step 1: Deactivate the Virtual Environment (If Active)

If you have activated the virtual environment, deactivate it first:

```bash
deactivate
```

### Step 2: Delete the Project Directory

Delete the entire project directory where your Django project resides. You can use the following command:

```bash
rm -rf myproject
```

This will remove the project directory along with all its contents, including any apps, settings, and migrations.

### Step 3: Delete the Virtual Environment (Optional)

If you created a virtual environment specifically for the project, you can delete that as well. Assuming your virtual environment is named `myenv`, run:

```bash
rm -rf myenv
```

This will remove the virtual environment folder and all its contents.
