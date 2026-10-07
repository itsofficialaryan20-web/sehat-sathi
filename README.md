# Sehat Sathi

A Vercel-ready React + TypeScript prototype for explaining printed blood-test reports in simpler language.

## Run locally

```bash
npm install
npm run dev
```

Open the local URL shown by Vite.

## Build for Vercel

```bash
npm run build
```

Vercel can deploy this project directly. Framework preset: **Vite**. Build command: `npm run build`. Output directory: `dist`.

## Prototype scope

- Responsive, accessible healthcare UI.
- Upload validation for PDF/JPG/PNG/WebP and 10 MB limit.
- Upload → processing → editable OCR review → explanation flow.
- Demo report mode with clearly labeled sample data.
- Browser speech synthesis with language selector when supported.
- Curated FAQ and privacy/medical safety messaging.
- No account, database, cloud storage, or external AI service.

### OCR limitation

The frontend currently uses a **clearly labeled prototype/demo extraction result** after an uploaded file is accepted. It does not pretend that the displayed sample values came from the uploaded report. For production, connect the processing step to a Python FastAPI service using OpenCV + Tesseract OCR + regex/RapidFuzz and return confidence values and source ranges. Do not send health data to an external AI service without explicit consent.

## Vercel deployment

1. Push this folder to GitHub.
2. Import the repository into Vercel.
3. Select Vite (or leave auto-detection).
4. Build command: `npm run build`.
5. Output directory: `dist`.
6. Deploy.

## Medical safety

Sehat Sathi is an educational explanation tool, not a diagnostic service. It does not prescribe, recommend medication changes, or replace a qualified healthcare professional. Production use requires clinical review, validated OCR, privacy/security review, and appropriate regulatory assessment.
