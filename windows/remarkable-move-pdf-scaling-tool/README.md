# User Guide — Remarkable™ Device Screen Dimension PDF Scaling Tool

This application helps you prepare PDFs for comfortable reading on **reMarkable™ Paper Pro Move** and **reMarkable™ Paper Pro** tablets. It resizes and optimizes your PDF files so that text, margins, and fonts display clearly on **reMarkable™ Paper Pro Move** and **reMarkable™ Paper Pro** screens.


---

## 1. Using the Software

Choose the correct version for your specific machine operating system (Windows, MacOS) from the folders above.

### Step 1 — Upload a PDF
- Choose your PDF file using the upload button.
- Large files are supported (up to 500 MB and 5000 pages).

### Step 2 — Select Target Device
- **Paper Pro Move**: 954 × 1695 px  
- **Paper Pro**: 1620 × 2160 px  
- Width and height fields update automatically.

### Step 3 — Choose Options
- **Preserve Aspect Ratio** – keeps proportions correct.  
- **Use Document Margins** – respects original page margins.  
- **Optimize for Reading** – enlarges text slightly for clarity.  
- **Adjust Line Spacing** – ensures balanced text layout.  
- **Scale Fonts** – resizes embedded fonts to match screen size.  
- **Add Page Numbers** – inserts centered numbers at bottom.

### Step 4 — Customize Fonts and Margins (optional)
- Pick font family (Serif, Sans, Monospace).
- Adjust font sizes and page margins if needed.

### Step 5 — Process and Download
- Click **Process**.  
- Wait until the conversion finishes.  
- Download and transfer it to your reMarkable device.

---

## 4. Activation & Testing Duration

- The software requires an activation code tied to your machine ID.  
- Activation codes provide limited-time access (30 days).  
- Full activation removes restrictions.  

---

## 5. API Quick Guide

For advanced users or integration with other tools:

### Upload & Process (Multipart Example)
```bash
curl -X POST "http://127.0.0.1:8000/api/process" \
  -F "inputFile=@/path/to/mydoc.pdf" \
  -F "targetDevice=remarkable-paper-pro-move" \
  -F "preserveAspectRatio=true" \
  -F "addPageNumbers=true"
```

The processed file will appear in `/uploads/`.

---

## 6. Tips for Best Results
- Use **Optimize for Reading** for books and long-form text.  
- For scanned documents, enable **Preserve Aspect Ratio** to avoid distortion.  
- If fonts don’t look right, check that the chosen family exists on your system (e.g., install **Noto Sans**).  
- Large files may take time; processing happens in batches.

---

## 7. Troubleshooting

- **Activation error** → Ensure the code matches your displayed Machine ID.  
- **Fonts missing** → Install or choose a different font family.  
- **Output unreadable** → Try disabling “Preserve Aspect Ratio” or reducing margins.  
- **403 error on API** → Activate the app first.  

---

## 8. Support

For activation codes or assistance, use the instructions shown in the activation dialog, or send an email to: info@rmppmove-tools.org  
