# Running Flask in a Virtual Environment

## Overview
In this step, we set up a virtual environment for Flask, installed Flask, and ran a basic Flask app.

## Steps

### 1. Create a Virtual Environment
We created a virtual environment to isolate dependencies:
```bash
python -m venv venv
```

### 2. Activate the Virtual Environment
We activated the virtual environment to work within it:
```bash
source venv/bin/activate  # For Linux/Mac
```

### 3. Install Flask
We installed Flask within the virtual environment:
```bash
pip install Flask
```

### 4. Write a Simple Flask App
We created a file named `app.py` with the following content:
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return "Hello, World!"

if __name__ == '__main__':
    app.run(debug=True)
```

### 5. Run the Flask App
We ran the Flask app:
```bash
python app.py
```

- The app started on `http://127.0.0.1:5000`, displaying "Hello, World!" when accessed.

### 6. Deactivate the Virtual Environment
After finishing, we deactivated the virtual environment:
```bash
deactivate
```

---

## Why These Steps?
1. **Virtual Environment**: Keeps dependencies isolated and avoids system-wide conflicts.
2. **Flask Installation**: Ensures Flask is installed only in the relevant environment.
3. **Basic App**: Verifies Flask is working and sets up a foundation for development.

---
