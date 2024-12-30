# RealTime-Gossips

RealTime-Gossips is a real-time chat application built using Django. It leverages HTMX for user interactivity and uses an ASGI server(Daphne) to upgrade to WebSockets. The app also utilizes Channel Layers to handle simultaneous communication among many users and uses Redis as an in-memory datastore with caching for fast sending and receiving of messages.

## Features

- **Online Tracker with WebSockets**: Tracks online status of users in real-time.
- **Private Chat**: Allows private messaging between individual users.
- **Public Chat**: Enables messaging between all users of the app.
- **Group Chat**: Facilitates chat between selected groups of users.
- **Live Activity Monitoring**: Monitors user activity in real-time.
- **Real-time File Sending**: Supports sending files in real-time.

## Installation

To install and set up the project locally, follow these steps:

1. **Clone the repository**:
   ```sh
   git clone https://github.com/SohamD242/RealTime-Gossips.git
   cd RealTime-Gossips

2. **Create a virtual environment**:
   ```sh
   python -m venv venv
   source venv\Scripts\activate  # On Mac use `venv/bin/activate`

3. **Install dependencies**:
   ```sh
   pip install -r requirements.txt

4. **Run migrations**:
   ```sh
   python manage.py migrate

5. **Start the Django server**:
   ```sh
   daphne -u /tmp/daphne.sock config.asgi:application

# Usage
1. Open your browser and navigate to http://localhost:8000.
2. Register a new user or log in with existing credentials.
3. Start chatting in public, private, or group chats.
4. Monitor live activities and send files in real-time.
