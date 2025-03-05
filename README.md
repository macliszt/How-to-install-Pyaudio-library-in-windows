
# **How to Install PyAudio on Windows (Resolving Python Version Conflicts)**  

After installing Python **3.13**, I encountered an issue where my system still defaulted to an older version (**Python 3.7.9**). This caused conflicts when setting up virtual environments and installing packages like **PyAudio**.  

This guide provides a **step-by-step** solution to:  
✅ Checking installed Python versions  
✅ Updating system **PATH** variables  
✅ Ensuring Python **3.13** is the default version  
✅ Creating a virtual environment with **Python 3.13**  
✅ Installing **PyAudio** from a local `.whl` file  

By following these steps, you can resolve similar **Python version conflicts** and ensure a successful installation of **PyAudio**. 🚀  

---

## **1. Download and Install Python 3.13**  
📥 **Download Python 3.13.2 from the official website:**  
🔗 [Python 3.13.2 Download](https://www.python.org/downloads/)  

### **During installation, check the box:**  
✅ **"Add Python to PATH"**  

🔄 **Restart your system after installation.**  

---

## **2. Verify Python Installation**  
Open the **Command Prompt (cmd or PowerShell)** and run:  
```sh
python --version
```
✅ **Expected Output:** `Python 3.13.x`  

---

## **3. Set Up a Virtual Environment**  
If you had an old virtual environment, **delete it** and create a new one:  
```sh
deactivate  # If inside an old virtual environment
rm -r myenv  # Delete old virtual environment
python -m venv venv  # Create a new virtual environment with Python 3.13
venv\Scripts\activate  # Activate the virtual environment
python --version  # Should now show Python 3.13
```
✅ **Your virtual environment is now set up!**  

---

## **4. Install PyAudio from a Local Wheel (.whl) File**  
Download the file from th repository
If you downloaded a **.whl file**, install it using:  
```sh
pip install "C:\Path\to\your\pyaudio.whl\PyAudio-0.2.14-cp313-cp313-win_amd64.whl"
```
⚠ **Ensure the path is correct before running the command.**  

---

## **5. Verify PyAudio Installation**  
### **Method 1: Check Installed Packages**
```sh
python -m pip show pyaudio
```
🔍 **This should display PyAudio package details.**  

### **Method 2: Import PyAudio in Python**
```sh
python
```
Then, type:  
```python
import pyaudio
print(pyaudio.__version__)  # Should print the installed version
```
✅ If there are **no errors**, PyAudio is successfully installed!  

