# Architecture

## System Architecture

ChainGuard AI uses a simple layered architecture. The user interacts with the dashboard, which communicates with the backend. The backend handles shipment, fleet, route, and temperature-related operations and connects with the required services.

```text
User / Browser
      ↓
Frontend - React
      ↓
Backend - FastAPI
   ↙    ↓      ↘
watsonx.ai  PostgreSQL  Slack Webhook

## Components

Frontend – React: Provides the dashboard and user interaction.
Backend – FastAPI: Handles business logic and connects the different components.
AI / ML – watsonx.ai: Provides the planned AI-powered logistics assistant and inference support.
Database – PostgreSQL: Stores operational data such as shipments, fleet, routes, and sensor information.
Notifications – Slack Webhook: Used for sending operational alerts and notifications.

## Data Flow

1.The user interacts with the ChainGuard dashboard.
2.The frontend sends requests to the FastAPI backend.
3.The backend processes shipment, fleet, route, and temperature data.
4.Relevant data can be sent to the AI service for analysis.
5.The backend generates priorities, recommendations, alerts, and explanations.
6.Results are displayed to the user through the dashboard.

## Security Considerations

Keep API keys and credentials in environment variables.
Do not commit sensitive credentials to GitHub.
Validate user inputs and API requests.
Use secure communication between system components.

## Scalability Notes

The architecture can be scaled by connecting live TMS, GPS, carrier, weather, and IoT data sources. The AI layer can also be expanded for predictive disruption detection and more advanced logistics recommendations.
