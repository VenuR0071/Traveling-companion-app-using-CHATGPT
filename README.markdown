# Traveling Companion App using ChatGPT

The Traveling Companion App is a React Native mobile application that provides real-time travel assistance and personalized recommendations using ChatGPT (via OpenAI API). It helps travelers by answering queries, offering destination suggestions, and enhancing their travel experience through AI-driven guidance. The app uses Express for the backend API and MongoDB to store user data and preferences, ensuring a tailored experience.

## Project Goals

- Provide real-time travel assistance using ChatGPT for answering user queries (e.g., "What are the best places to visit in Tokyo?").
- Offer personalized recommendations based on user preferences stored in MongoDB.
- Build a cross-platform mobile app with React Native for iOS and Android.
- Ensure a scalable backend with Express to handle API requests and ChatGPT integration.

## Tech Stack

### Frontend
- **React Native**: Cross-platform framework for building the mobile app.
- **Axios**: For making API requests to the backend.

### Backend
- **Express**: Node.js framework for building the API to handle user requests and ChatGPT integration.
- **MongoDB**: NoSQL database to store user profiles, travel history, and preferences.
- **Mongoose**: ODM for MongoDB to manage database interactions.
- **OpenAI API**: Provides ChatGPT functionality for AI-driven responses.

### Other Tools
- **Node.js and npm**: For managing backend dependencies and running the server.
- **Git**: For version control.

## Prerequisites

- **Node.js 16+ and npm**: For running the backend and React Native CLI.
- **MongoDB**: Local installation or a cloud instance (e.g., MongoDB Atlas).
- **OpenAI API Key**: Required for ChatGPT integration (sign up at [OpenAI](https://platform.openai.com/)).
- **React Native Environment**: Set up for iOS/Android development (see [React Native docs](https://reactnative.dev/docs/environment-setup)).
- **Git**: For cloning the repository.

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/traveling-companion-app.git
   cd traveling-companion-app
   ```

2. **Set Up the Backend**
   - Navigate to the backend directory:
     ```bash
     cd backend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Create a `.env` file in the `backend` directory with the following:
     ```env
     MONGODB_URI=mongodb://localhost:27017/travelcompanion
     OPENAI_API_KEY=your-openai-api-key
     PORT=5000
     ```
   - Start the backend server:
     ```bash
     npm start
     ```

3. **Set Up the Frontend**
   - Navigate to the frontend directory:
     ```bash
     cd frontend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the React Native app:
     ```bash
     npx react-native run-android  # For Android
     npx react-native run-ios      # For iOS
     ```

4. **Configure MongoDB**
   - Ensure MongoDB is running locally or use a cloud instance.
   - Update `MONGODB_URI` in the backend `.env` file if using a different MongoDB instance.

## Running the App

1. **Start the Backend Server**
   Ensure the Express server is running:
   ```bash
   cd backend
   npm start
   ```
   The server will run on `http://localhost:5000`.

2. **Launch the Mobile App**
   Run the React Native app on your device/emulator:
   ```bash
   cd frontend
   npx react-native run-android  # or run-ios
   ```

3. **Interact with the App**
   - Open the app on your device/emulator.
   - Enter travel-related queries (e.g., "Suggest a 3-day itinerary for Paris").
   - Receive AI-driven responses powered by ChatGPT.
   - Save preferences (e.g., favorite destinations) to MongoDB for personalized recommendations.

## Project Structure

```
traveling-companion-app/
├── backend/
│   ├── server.js           # Express server setup and API routes
│   ├── models/             # Mongoose schemas for MongoDB
│   ├── routes/             # API routes for user and ChatGPT interactions
│   ├── package.json        # Backend dependencies
│   ├── .env               # Environment variables (API keys, MongoDB URI)
├── frontend/
│   ├── App.js             # Main React Native app component
│   ├── src/               # App screens and components
│   ├── package.json       # Frontend dependencies
├── README.md              # Project documentation
```

## Usage

- **Ask Travel Questions**: Input queries like "Where should I eat in Rome?" to get recommendations from ChatGPT.
- **Save Preferences**: Store your travel preferences (e.g., preferred cuisines, destinations) in MongoDB.
- **Get Personalized Recommendations**: Receive suggestions tailored to your saved preferences and past queries.

## Limitations and Future Improvements

- **Current Limitations**:
  - This is a conceptual structure; code implementation is pending.
  - OpenAI API costs may apply for ChatGPT usage.
  - Limited error handling and UI design (to be developed).
- **Future Improvements**:
  - Add offline support for travel guides.
  - Integrate maps and geolocation for real-time navigation.
  - Enhance UI/UX with React Native components (e.g., chat bubbles, itinerary planner).
  - Implement user authentication for secure data storage.

## Troubleshooting

- **Backend Not Connecting to MongoDB**:
  - Verify `MONGODB_URI` in `.env` and ensure MongoDB is running.
- **ChatGPT Responses Fail**:
  - Check `OPENAI_API_KEY` in `.env` and ensure your OpenAI account has credits.
- **App Not Running**:
  - Ensure React Native environment is set up correctly (check logs for errors).
  - Run `npm install` in both `frontend` and `backend` directories.

## Contributing

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License

MIT License. See [LICENSE](LICENSE) for details.

## Contact

For questions or feedback, open an issue on GitHub or contact the repository owner.