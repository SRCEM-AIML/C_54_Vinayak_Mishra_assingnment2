## 🎓 StudentProject
## 📌 Project Overview
## Build a Multi-App Django Project and Deploy with Docker
## 🚀 Getting Started
## 1️⃣ Clone the Repositor
``` 
git clone https://github.com/vinayakmishra-11/StudentProject.git
cd StudentProject
```
## 2️⃣ Set Up a Virtual Environment (Recommended)
```
python -m venv venv  
source venv/bin/activate  # (Linux/macOS)  
venv\Scripts\activate     # (Windows)

```
## 3️⃣ Install Dependencies
```
pip install -r requirements.txt
```
## 4️⃣ Run the Django Server Locally
```
python manage.py runserver
```
🔗 The app should now be accessible at http://127.0.0.1:8000/
## 🐳 Running with Docker
## 1️⃣ Build the Docker Image
```
docker build -t studentproject .
```
## 2️⃣ Run the Container
```
docker run -p 8000:8000 studentproject
```
🔗 The application will be available at http://localhost:8000/
## 🔄 CI/CD with Jenkins
### 1️⃣ Ensure Jenkins is Running
```
net start jenkins  # Windows  
sudo systemctl start jenkins  # Linux
```
## 2️⃣ Push Code to GitHub to Trigger Jenkins Pipeline
```
git add .
git commit -m "Initial commit"
git push origin main
```
✅ Ensure your Jenkinsfile is correctly set up in your repository.

## 📌 Docker Hub Image
You can pull the prebuilt Docker image using:

```
docker pull vinayakmishra11/studentproject
```
🔍 Find the Docker image here: Docker Hub

❗ Troubleshooting
🔹 Check logs for errors:

```
docker logs <container_id>
```
🔹 Verify that ports are correctly mapped.
🔹 Ensure Jenkinsfile and Dockerfile are correctly configured.


