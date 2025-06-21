# 🚀 InstaHost

**InstaHost** is a modern web tool designed to make static website deployment effortless. Upload your HTML, CSS, and JavaScript files (or a zipped archive) via a simple web interface, and get a public AWS S3 link instantly—no DevOps required.

---

## 🌟 What Does InstaHost Do?

- **Instant Hosting:** Upload your static site and get a shareable, public URL in seconds.
- **No Servers, No Hassle:** Powered by AWS S3's static site hosting—no server maintenance, just pure hosting.
- **History:** See all your previous uploads and access their live links.
- **Simple & Secure:** All hosting is done on your own S3 bucket using IAM credentials; your data stays yours.
- **Free Tier Friendly:** Designed to work smoothly within AWS Free Tier limits, so you can host sites at zero cost (within AWS usage).

---

## 🗂️ Folder Structure

```
instahost/
├── backend/       # Spring Boot backend (Java)
│   ├── src/
│   │   └── main/
│   │       ├── java/
│   │       │   └── com/instahost/
│   │       │       ├── InstaHostApplication.java
│   │       │       ├── controller/
│   │       │       │   └── UploadController.java
│   │       │       ├── service/
│   │       │       │   └── S3Service.java
│   │       │       └── config/
│   │       │           └── CorsConfig.java (if needed)
│   │       └── resources/
│   │           └── application.properties
│   └── pom.xml
├── frontend/      # React frontend (JavaScript)
│   ├── src/
│   │   ├── App.js
│   │   ├── UploadForm.js
│   │   └── History.js
│   ├── public/
│   ├── package.json
│   └── ...
└── README.md
```

---

## ⚙️ How to Set Up the Project

### 1. Backend: Spring Boot Setup

**a. Create the Spring Boot project**

- Using [Spring Initializr](https://start.spring.io/):
  - Project: Maven
  - Language: Java
  - Packaging: Jar
  - Java: 17+
  - Dependencies: Spring Web

**b. Directory Setup**

```bash
mkdir backend
cd backend
# Use Spring Initializr or your IDE to generate the project here
```

**c. Add AWS SDK dependency**  
Add to your `pom.xml`:

```xml
<dependency>
  <groupId>software.amazon.awssdk</groupId>
  <artifactId>s3</artifactId>
</dependency>
```

**d. Place the backend code in the structure as described above.**

---

### 2. Frontend: React App Setup

**a. Create the React app**

```bash
npx create-react-app frontend
cd frontend
npm install axios react-dropzone
```

**b. Place the frontend code in the structure as described above.**

---

## 🛠️ How to Use InstaHost

1. **Start the Backend**
   - Set AWS credentials as environment variables (`AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`)
   - In `/backend`:
     ```bash
     ./mvnw spring-boot:run
     ```
2. **Start the Frontend**
   - In `/frontend`:
     ```bash
     npm start
     ```
   - Open [http://localhost:3000](http://localhost:3000)

3. **Upload Your Site:**  
   - Drag and drop your HTML/CSS/JS files or a ZIP archive via the InstaHost web UI.
4. **Get Your Link:**  
   - Receive an instant public URL to access or share your live site.
5. **Check Upload History:**  
   - Easily view all your previously deployed sites and their URLs.

---

## 💡 Use Cases

- Portfolios and resumes  
- Event or hackathon landing pages  
- Demos and proof-of-concept apps  
- Quick static site sharing with team or clients  

---

## 🌍 Public URL Example

```
https://your-bucket-name.s3.amazonaws.com/your-folder/index.html
```

---

## 🏷️ License

MIT License

---

## 👨‍💻 Creator

- [Ashish73653](https://github.com/Ashish73653)

---
