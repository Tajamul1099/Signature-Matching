# ✍️ Signature Matching System

## 📌 Overview

The **Signature Matching System** is a desktop-based application that compares two handwritten signatures and determines their similarity using image processing techniques.

The system leverages **OpenCV** and **Structural Similarity Index (SSIM)** to analyze and validate whether two signatures match based on a predefined threshold.

---

## 🚀 Features

* 📸 Capture signatures using webcam
* 📂 Upload signature images from local system
* 🔍 Compare two signatures with similarity score
* ✅ Displays **Match / Not Match** result
* 📊 Shows similarity percentage
* 🖥️ Simple and interactive GUI using Tkinter

---

## 🧠 How It Works

1. User selects or captures two signature images
2. Images are converted to grayscale
3. Images are resized to a standard size (300x300)
4. SSIM algorithm calculates similarity
5. Result is compared with threshold (85%)
6. System displays:

   * ✅ Match (if similarity > 85%)
   * ❌ Not Match (if similarity ≤ 85%)

---

## 🖼️ Application Screenshots

### ✅ Successful Match

![Image](https://images.openai.com/static-rsc-4/zwN-EKyGrRiJjTW1MY2PSJYlL3ofNFtg6_ccw2hA9HXAkcIuqnMtckW1fbTiy6G68tux1cR6O1CtJ_fyaIBX2n7Jl_WPtLhhGAyU35hFRvVNcmV0qmpkof-LYR0nub1CMhmXMnLT8riQ1LyeVPkHWC2dEgBfqjjK3IqnEefifxWHiLwxKmvjb472K4VNWXCX?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/7ZwRw_zS2yw_TFTGXFsYkdh9NmYCKpHfWXSeIM3iMscDYFgLz2mzqo15QObiW0VrIQj-7B-OaStOO3Jre-ktSoH1ly1mLeG2hMVCrTvg4xg6rQFntMvXX2rSwmvZ22s_8_Y6FNe1OnKK_YKFZ-_Y2CBfQm5mNXKg8ETxG7HQUU47A9KWSHLOXzvDJVYRFJNH?purpose=fullsize)

### ❌ Failed Match

![Image](https://images.openai.com/static-rsc-4/6FczPsu9aaYX8o-yKa1cbMuTADQZyJqxdLHwdnWpqXTVtmph1iGVSdF9-u6JNdEFl8tAlVP4FHVvF-6LfmWju04ZDExJCzc4Q7lLho2_S3ak5GYbalxPhiqlix5Bqq5phRkFfIx_95IwIOwxBGzK7GVRRVgXHEWl7JAtI3FxobqukPSF6UzIf-76l0DwsF0W?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/7ZwRw_zS2yw_TFTGXFsYkdh9NmYCKpHfWXSeIM3iMscDYFgLz2mzqo15QObiW0VrIQj-7B-OaStOO3Jre-ktSoH1ly1mLeG2hMVCrTvg4xg6rQFntMvXX2rSwmvZ22s_8_Y6FNe1OnKK_YKFZ-_Y2CBfQm5mNXKg8ETxG7HQUU47A9KWSHLOXzvDJVYRFJNH?purpose=fullsize)

---

## 🛠️ Tech Stack

* **Python**
* **Tkinter** (GUI)
* **OpenCV (cv2)** – Image processing 
* **Scikit-image (SSIM)** – Similarity calculation 
* **NumPy**

---

## 📂 Project Structure

```
📁 Signature-Matching
│── main.py              # GUI application
│── signature.py         # Image comparison logic
│── temp/                # Captured images (auto-created)
│── README.md            # Project documentation
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/signature-matching.git
cd signature-matching
```

### 2️⃣ Install Dependencies

```bash
pip install opencv-python scikit-image numpy
```

### 3️⃣ Run Application

```bash
python main.py
```

---

## 📊 Core Logic

### 🔹 Signature Comparison Function

The system reads two images, processes them, and computes similarity:

```python
similarity_value = ssim(img1, img2) * 100
```

* Images are converted to grayscale and resized before comparison
* Output is a percentage value representing similarity

---

## 🎯 Threshold Logic

* **Threshold = 85%**
* If similarity > 85 → ✅ Match
* Else → ❌ Not Match

This logic is implemented in the system: 

---

## 📈 Example Output

| Scenario            | Similarity | Result      |
| ------------------- | ---------- | ----------- |
| Same Signature      | 100%       | ✅ Match     |
| Different Signature | 62.61%     | ❌ Not Match |

---

## 💡 Use Cases

* Bank signature verification
* Document authentication
* Identity validation systems
* Fraud detection

---

## ⚠️ Limitations

* Sensitive to image quality and lighting
* Does not handle rotated/skewed signatures
* No advanced feature extraction (basic SSIM only)

---

## 🔮 Future Enhancements

* Add **deep learning model for signature recognition**
* Improve accuracy using **feature extraction (SIFT/ORB)**
* Add **signature database storage**
* Deploy as a **web application**

---

## 👨‍💻 Author

**Mohammed Tajamul Hussain**
📊 Data Analyst | Python | SQL | Power BI

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share it!

---
