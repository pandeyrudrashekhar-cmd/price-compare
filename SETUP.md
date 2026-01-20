# Setup Instructions

## Backend Setup

1. **Navigate to backend folder:**
```bash
cd c:\Users\Rudra shekhar pandey\OneDrive\Desktop\ninja\backend
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Run the backend server:**
```bash
python app.py
```

The backend will start on `http://localhost:5000`

## Frontend Setup

1. **Navigate to frontend folder (in a new terminal):**
```bash
cd c:\Users\Rudra shekhar pandey\OneDrive\Desktop\ninja\frontend
```

2. **Install dependencies:**
```bash
npm install
```

3. **Start the development server:**
```bash
npm run dev
```

The frontend will open at `http://localhost:3000`

## How It Works

1. User enters a product name in the search bar
2. Frontend sends request to backend (`/api/search` endpoint)
3. Backend starts 3 parallel tasks (Amazon, Flipkart, Myntra) via MobileRun API
4. Frontend polls backend for task status every 5 seconds (`/api/task/<task_id>`)
5. When all tasks complete, prices are displayed and compared
6. Best deal is highlighted

## Architecture

- **Frontend**: React + Tailwind CSS - handles UI and user interaction
- **Backend**: Flask + CORS - acts as proxy to MobileRun API, keeps API key secure
- **External API**: MobileRun API - executes mobile app automation tasks

## Important Notes

- ✅ API key is now secure (only in backend)
- ✅ CORS issues are resolved
- ✅ No external dependencies like lucide-react
- ✅ Clean separation of concerns
