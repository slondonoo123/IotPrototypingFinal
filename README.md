# IotPrototypingBackend
This repository hosts PetTracker, the final project for the IoT Prototyping course. Inside, you’ll find the full integration pipeline between The Things Network (TTN) and Microsoft Azure, along with a React frontend and a Node.js backend that together form the application's user interface and API.

Backend Libraries
Library	Purpose
express	REST API server
cors	Enable cross-origin requests
dotenv	Load environment variables
@azure/cosmos	Read/write Cosmos DB documents
node-fetch / global fetch	Send HTTP requests to TTN

Azure Function Libraries
Library	Purpose
@azure/functions	Azure Functions runtime
@azure/cosmos	Storage of decoded sensor data

Frontend (React)
Library	Purpose
react	UI rendering
axios	HTTP requests to backend
chart.js (if used)	Visualizing data
react-router	Navigation
react	Core React framework for building UI components
react-native	Native mobile UI framework used for building screens, styles, and components
expo platform	Allows running the app in Expo environment
expo-image	High-performance image component for React Native
@react-navigation/native	Used for navigating between screens in the app
useFocusEffect	Hook that triggers re-renders when screen becomes active
@expo/vector-icons (Ionicons)	Full icon pack used for buttons, indicators, and UI elements
react-native-circular-progress	Circular progress animation used for displaying activity or battery levels

Prerequisites
1. Environment Variables
Create a .env file with:
COSMOS_ENDPOINT=xxxx
COSMOS_KEY=xxxx
DATABASE_ID=IoTMessages
CONTAINER_ID=DeviceData
TTN_APP_ID=xxxx
TTN_API_KEY=xxxx
PORT=3001

2. Azure Requirements
Azure Cosmos DB account
Database: IoTMessages
Container: DeviceData
Event Hub input configured for TTN traffic
Function App deployed and connected to Event Hub

3. The Things Network (TTN)
Application created
Device added
Payload decoder configured
Downlink API key created

4. Backend Installation & Run
npm install
node server.js

5. Frontend Installation & Run
npm install
npm start

6. Folder Contents
/backend
/react-app
/azure-function
README.md
