# Week 01 - Basic FastAPI Application Example

This repository contains a minimal FastAPI application designed to help you set up and verify your Python development environment for the unit. It serves as a simple "hello world" to ensure `Python`, `pip`, `venv`, `FastAPI`, and `Uvicorn` are installed and working correctly.

## Prerequisites

Before you begin, ensure you have the following installed:

- `Python`

- `pip` (Python package installer, usually comes with Python)

- `venv` (Python module for creating virtual environments, usually comes with Python)

## Setup and Run Instructions

Follow these steps to get the basic FastAPI application running on your local machine:

1. Clone the Repository:
   If you haven't already, clone the unit's example code repository to your local machine:

```bash
git clone <URL_TO_YOUR_UNIT_GITHUB_REPOSITORY>
```

2. Then navigate into the `week01` directory:

```bash
cd week01
```

3. Create and Activate a Python Virtual Environment:

It's best practice to use a virtual environment to manage project dependencies.

```bash
# Create the virtual environment
python -m venv .venv

# Activate the virtual environment
# On macOS/Linux:
source ./.venv/bin/activate
# On Windows (Command Prompt):
# .\.venv\Scripts\activate.bat
# On Windows (PowerShell):
# .\.venv\Scripts\Activate.ps1
```

You should see `(.venv)` prefixing your terminal prompt, indicating the virtual environment is active.

4. Install Dependencies:

With your virtual environment activated, install the required Python packages:

```bash
pip install -r requirements.txt
```

5. Update Your Information in `main.py`

Open the `main.py` file in your VS Code editor. Locate the get_student_info endpoint and update the placeholder information (<YOUR_NAME>, <YOUR_STUDENT_ID>, <YOUR_CAMPUS>) with your actual details. Save the file after making these changes.

6. Run the FastAPI Application:

Once dependencies are installed, you can start the FastAPI application using Uvicorn:

```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

- `main:app`: Specifies that Uvicorn should look for an app object (your FastAPI instance) within the app.py file.

- `--reload`: Enables auto-reloading of the server on code changes (useful for development).

- `--host 0.0.0.0`: Makes the application accessible from outside localhost (e.g., from other devices on your local network, or from Docker containers if you later integrate).

- `--port 8000`: Specifies the port the application will listen on.

7. Access the Application in Your Browser:

Open your web browser and navigate to the following URLs:

- Root Endpoint: `http://localhost:8000/`

- Student Info Endpoint: `http://localhost:8000/student_info`

Congratulations! Your basic FastAPI development environment is set up and working.
