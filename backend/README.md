# FastAPI Backend for AI Stock Assistant

## Local Development

Install dependencies:
```bash
pip install -r requirements.txt
```

Run locally:
```bash
uvicorn app.main:app --reload
```

## Deployment (Recommended: Railway)

1. Go to [Railway](https://railway.app).
2. Create a new project, and link this repository (or import only the `backend` folder).
3. Ensure Railway detects a Python project and sets the start command to:
    ```
    uvicorn app.main:app --host 0.0.0.0 --port $PORT
    ```
4. Deploy.
5. After deployment, get your public Railway URL (e.g., `https://your-backend.up.railway.app`).

## For Render, Heroku, or Others

- Make sure to use the `Procfile` and `requirements.txt`.
- Set the start command to:
    ```
    uvicorn app.main:app --host 0.0.0.0 --port $PORT
    ```

---

### After Deploying

- Copy the public URL of your backend.
- In your Vercel frontend project, add an environment variable:
    - Key: `VITE_API_URL`
    - Value: (your backend URL)
- Redeploy the frontend on Vercel.

---