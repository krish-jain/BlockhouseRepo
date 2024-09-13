For the backend, you’ll go to

1. Go to chartbackend
2. Install the required dependencies using pip install -r requirements.txt or using npm
3. Run the Django server using python manage.py runserver ( http://localhost:8000 ). 
For the frontend (Next.js):

1. Navigate to the frontend folder.
2. Install the dependencies using npm install.
3. Start the Next.js development server using npm run dev. This will start the frontend server at http://localhost:3000.

Make sure both servers are running simultaneously. You can access the frontend at http://localhost:3000. This is where you will see the graphs.

For the backend:

Django: the web framework used for the backend.
Django REST Framework: for building the API.
django-cors-headers: to handle CORS for cross-origin requests between the frontend and backend.

For the frontend:

Next.js: the React framework for building the frontend.
Axios: used for making API requests to the Django backend.
react-chartjs-2: used for rendering Line, Bar, and Pie charts.
react-financial-charts: used for rendering the Candlestick chart.
Chart.js: the core charting library used with react-chartjs-2.
d3-scale: used for time-based scaling in the Candlestick chart.

For the backend, the Django API serves hardcoded data for the charts via simple API endpoints. Each chart type has its own endpoint that provides the necessary data (e.g., /api/candlestick-data/, /api/line-chart-data/). For the frontend, the application uses Next.js and React to fetch data from the Django API and render charts using react-chartjs-2 for most charts, and react-financial-charts for the Candlestick chart. Axios is used for making the API requests. The goal was to keep the code modular and maintainable while allowing dynamic data fetching from the backend.