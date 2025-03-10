# fMRI Cluster Analysis Web Application

This application leverages Streamlit, AFNI, and Deep Research Sonar model from Perplexity to facilitate anatomical labeling and interpretation of fMRI cluster data.

![fMRI Cluster Analysis](AIclusters.png)

---

## ⚙️ How it works

1. **Cluster File Input**:
   - Accepts `.1D` files generated by AFNI or `.m` files from SPM (converted internally).

2. **Atlas-Based Anatomical Labeling**:
   - Uses standard atlases (Julich_MNI2009c, FS.afni.MNI2009c_asym) provided by AFNI.
   - Label clusters using `whereami` tool from AFNI.

3. **Detailed interpretation** generated by the **Deep Research Sonar model from Perplexity**.

---

## 📌 **Prerequisites**

### AFNI Installation

This app requires AFNI installed on your local system.

- [**Install AFNI**](https://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/index.html)

Verify installation:
```bash
whereami -help
```

### Perplexity API Key

To use Perplexity’s Deep Research Sonar model for the automated cluster interpretation, you’ll need a Perplexity API key:
1. Go to https://www.perplexity.ai/settings/api and log in or sign up.
2. Generate your API key.
3. Provide this key in the application code 

---

## 🔧 Installation

### 1. Download the Repository or Clone it
```bash
git clone https://github.com/tdelavy/fMRI-ClusterAI.git
cd fMRI-ClusterAI
```

### 2. Install Dependencies
Create a Python environment (recommended) and install dependencies:

```bash
pip install -r requirements.txt
```

### 3. Set your OpenAI API Key

- Open the python file "AI.py" and replace `Add_Your_OpenAI_Key` with your actual OpenAI API key on line 13. 
You MUST have a paid version to use it.


### 4. Install Dependencies

Ensure you have Python 3.10+ installed. Then install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Streamlit App

To start the app locally:
Open your terminal and write:
```bash
cd path/to/fMRI-ClusterAI
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

