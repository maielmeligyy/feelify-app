# How to Run Feelify

This guide will walk you through setting up and running the Feelify app.

## Prerequisites

- Node.js 14+
- Python 3.8+
- Expo CLI
- iOS simulator or actual iOS device with Expo Go installed

## Setup Instructions

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Start the Flask server:
   ```bash
   python app.py
   ```

### Frontend Setup

1. Navigate to the app directory:
   ```bash
   cd feelify-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the Expo development server:
   ```bash
   npm start
   ```

4. Open on iOS simulator or scan the QR code with Expo Go on your device.

## Step 5: Using the App

1. When the app launches, you'll see the Camera screen asking you to record a video answering emotional questions.

2. After recording, you'll proceed to the Voice Recording screen to record audio responses.

3. Next, you'll be asked for your age and preferred music genre.

4. Finally, the app will analyze your emotions and generate a personalized Spotify playlist recommendation.

## Troubleshooting

- **Camera/Microphone Permission Issues**: Ensure you grant the necessary permissions when prompted.
- **Connection Errors**: Make sure your backend is running and the API URL is correctly set to your MacBook's IP address.
- **Hot Reloading**: If you make changes to the code, the app should automatically reload. If not, shake your iPhone and select "Reload" from the developer menu.

## Note for Development

By default, the app is configured to use mock data for playlist generation (no backend connection). To use the actual backend:

1. Open `screens/QuestionnaireScreen.js`
2. Find the line: `const useMockData = true;`
3. Change it to: `const useMockData = false;`

## Support

If you encounter any issues, please check the following:

1. Both the backend and frontend are running
2. Your iPhone and MacBook are on the same network
3. The API URL in QuestionnaireScreen.js points to your MacBook's IP address
4. All required permissions have been granted on your iPhone

For additional help, refer to the project's README files or contact the project maintainers. 