# Local Development Setup

## Prerequisites
- Python 3.8+
- Node.js and npm (for Vercel CLI if deploying)

## Running Locally

### 1. Backend API (FastAPI)
```bash
cd api
pip install -r requirements.txt
python main.py
```
The API will run on http://127.0.0.1:8000

### 2. Frontend (Static Files)
```bash
# Option 1: Use Python's built-in server
cd public
python -m http.server 3000

# Option 2: Use Node.js
npx serve public -l 3000
```
The frontend will run on http://localhost:3000

### 3. Access the Application
- Open http://localhost:3000 in your browser
- The frontend will connect to the API at http://127.0.0.1:8000

## Testing the API
```bash
# Test API endpoints
curl http://127.0.0.1:8000/
curl http://127.0.0.1:8000/students
curl "http://127.0.0.1:8000/predict/12345"  # Replace with actual student ID
```

## Deployment (when ready)
1. Deploy frontend to Vercel
2. Deploy API to Render
3. Update frontend environment variables with production URLs

## Troubleshooting
- Make sure both servers are running
- Check browser console for CORS or connection errors
- Ensure all required files (model.joblib, data.csv) are in the api/ directory
