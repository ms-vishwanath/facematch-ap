# 🧠 FaceMatch API – AWS Rekognition Face Upload & Search

A Node.js and Express.js API that integrates with **AWS Rekognition** to enable:

- ✅ Tamper-proof **face collection** and indexing
- 🔍 Intelligent **face search/matching**
- 📸 Bulk photo upload and listing of all stored face entries

Ideal for secure authentication systems, photo databases, or surveillance logs.

---

## 🚀 Features

- 📂 Upload multiple photos and index faces to Rekognition collection
- 🧠 Search by face image (real-time face comparison)
- 📋 Retrieve all indexed face metadata
- 💾 Uses AWS Rekognition for highly accurate facial matching

---

## 🛠️ Tech Stack

- **Node.js**
- **Express.js**
- **AWS Rekognition**
- **Multer** for handling file uploads

---

## 📦 API Endpoints

### `POST /upload-photos`
Upload and index multiple face photos into the Rekognition collection.

**Body:**
- `photos`: `multipart/form-data` array of images

---

### `POST /search-photo`
Search a single face photo against the indexed Rekognition collection.

**Body:**
- `photo`: `multipart/form-data` single image

---

### `GET /all`
Returns metadata or references of all indexed images (IDs, timestamps, etc.).

---

## 🧑‍💻 Setup Instructions

```bash
# 1. Clone the repo
git clone https://github.com/ms-vishwanath/facematch-api.git
cd facematch-api

# 2. Install dependencies
npm install

# 3. Configure AWS credentials
# either use ~/.aws/credentials or environment variables
export AWS_ACCESS_KEY_ID=your_access_key
export AWS_SECRET_ACCESS_KEY=your_secret_key
export AWS_REGION=your_aws_region

# 4. Start the development server
npm run dev


.
├── controllers/
│   ├── UploadPhotos.ts        # Handles photo uploads to AWS Rekognition
│   ├── SearchPhotos.ts        # Handles face comparison
│   └── GetAllImages.ts        # Lists indexed faces
├── routes/
│   └── PhotoRouter.ts         # Express router setup
├── server.ts                  # Entry point

MIT License © 2025 Vishwanath

‣慦散慭捴⵨灡�