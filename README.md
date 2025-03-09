# fMRI Cluster Analysis Web Application

This application leverages Streamlit, AFNI, and the OpenAI o1 model to facilitate anatomical labeling and interpretation of fMRI cluster data.

---

## ⚙️ How it works

1. **Cluster File Input**:
   - Accepts `.1D` files generated by AFNI or `.m` files from SPM (converted internally).

2. **Atlas-Based Anatomical Labeling**:
   - Uses standard atlases (Julich_MNI2009c, FS.afni.MNI2009c_asym) provided by AFNI.
   - Label clusters using `whereami` tool from AFNI.

3. **Detailed interpretation** generated by the **OpenAI o1-high model**.

---

## 📌 **Prerequisites**

### AFNI Installation

This app requires AFNI installed on your local system.

- [**Install AFNI**](https://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/index.html)

Verify installation:
```bash
whereami -help
```

---

## 🔧 Installation

### 1. Download the Repository or Clone it
```bash
git clone https://github.com/tdelavy/ClusterAI.git
cd ClusterAI
```

### 2. Install Dependencies
Create a Python environment (recommended) and install dependencies:

```bash
pip install -r requirements.txt
```

### 2. Set your OpenAI API Key

Replace `your-user-specific-key-here` with your actual OpenAI API key. You MUST have a paid version to use it.

- **macOS/Linux:**

Open your your shell configuration in your terminal and write:
```bash
nano ~/.zshrc
```
Add this line inside, save and quit:
```bash
export OPENAI_API_KEY="your-user-specific-key-here"
```

Write then this line to apply your changes:
```bash
source ~/.zshrc
```

- **Windows:**

Open Command Prompt and run:

```cmd
setx OPENAI_API_KEY "your-user-specific-key-here"
```

*(Restart your terminal or computer to apply changes.)*

### 2. Install Dependencies

Ensure you have Python 3.10+ installed. Then install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Streamlit App

To start the app locally:
Open your terminal and write:
```bash
cd path/to/ClusterAI
```
and run:
```bash
streamlit run AI.py
```

The app will open automatically in your web browser at:
```
http://localhost:8501
```

---

## 📂 Folder Structure

```
├── AI.py                 # Streamlit App
├── requirements.txt       # Python dependencies     
├── extract_spm_peaks.py         # Utility to convert SPM .m files
├── Julich_MNI2009c_Atlas.png
└── FS.afni.MNI2009c_asym_Atlas.png
```

---

