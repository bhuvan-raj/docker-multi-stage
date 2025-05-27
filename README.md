
# 🐳 Multi-Stage Dockerfile - Golang Example

This repository demonstrates the concept of **multi-stage Docker builds** using a simple Go application. The goal is to show the difference in image size between single-stage and multi-stage Docker builds.

---

## 📘 What is a Multi-Stage Dockerfile?

A **multi-stage Dockerfile** is a technique that uses multiple `FROM` statements to define multiple build stages. It helps to separate the build environment from the final runtime environment, reducing the image size by copying only the necessary artifacts into the final image.

---

## ❓ Why Use Multi-Stage Builds?

- ✅ **Smaller image size** (no compiler or build tools in the final image)
- ✅ **Faster deployment**
- ✅ **Improved security** (fewer attack vectors)
- ✅ **Cleaner, production-ready containers**

---

## 🔧 Steps to Run This Practical

### 📥 1. Clone the Repository
```bash
git clone https://github.com/bhuvan-raj/docker-multi-stage.git
cd docker-multi-stage
````

### 🧱 2. Build Single-Stage Docker Image

```bash
cd docker-single-stage\ build
```
```
docker build -t single-stage-app .
```

### 🔍 3. Check Image Size

```bash
docker images
```

Note the image size of `single-stage-app`.

---

### 🧱 4. Build Multi-Stage Docker Image

```bash
cd ..
```
```
docker build -t multi-stage-app .
```

### 🔍 5. Check Image Size Again

```bash
docker images
```

Compare the size of `multi-stage-app` with `single-stage-app`. The multi-stage image should be significantly smaller.

---

## 📂 Repo Structure

```
├── docker-single-stage build/
│   ├── Dockerfile
│   └── calculator.go
├── Dockerfile           # Multi-stage Dockerfile
├── calculator.go        # Source code
└── README.md
```

---

