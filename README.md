# Flask App Documentation

## Overview
This project is a basic Flask application designed to demonstrate web development with Python using the Flask framework. The application runs on Docker, allowing for portability and ease of deployment.

## Features
- Flask-based web application
- Dockerized for platform independence
- Environment variables for configuration
- Easy to set up and run locally

---

## Prerequisites

Before you start, ensure you have the following installed on your system:

1. [Python](https://www.python.org/downloads/) (version 3.8 or later)
2. [Docker](https://www.docker.com/)
3. [Git](https://git-scm.com/)

---

## Project Setup

### Step 1: Clone the Repository
Clone this repository to your local machine:
```bash
git clone git@github.com:<your-username>/<repository-name>.git
cd <repository-name>
```

### Step 2: Set Up a Virtual Environment (Optional but Recommended)
Create and activate a virtual environment:
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## Running the Application Locally

### Without Docker
1. Start the Flask application:
   ```bash
   python app.py
   ```
2. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

### With Docker
1. Build the Docker image:
   ```bash
   docker build -t flask-app .
   ```
2. Run the Docker container:
   ```bash
   docker run -d -p 5000:5000 flask-app
   ```
3. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

---

## Project Structure
```plaintext
project-directory/
|-- app.py              # Main Flask application file
|-- Dockerfile          # Docker configuration
|-- requirements.txt    # Python dependencies
|-- .gitignore          # Git ignore file
|-- venv/               # Virtual environment (excluded from Git)
```

---

## Deployment
To deploy this application, ensure Docker is installed on the target machine and follow the steps under the **With Docker** section.

---

## Troubleshooting

### Issue: `url_quote` ImportError
- Ensure you are using compatible versions of Flask and Werkzeug by updating your `requirements.txt`:
  ```plaintext
  Flask==2.1.2
  Werkzeug==2.1.2
  ```

### Issue: Docker Container Not Running
- Check logs using:
  ```bash
  docker logs <container_id>
  ```
- Ensure the correct ports are mapped.

### Issue: Permission Denied (Git Push)
- Ensure your SSH keys are correctly configured for GitHub. Refer to the [GitHub SSH guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

---

## Contributing
1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature-name"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a Pull Request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

