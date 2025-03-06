# Interactive Trivia Game

## Overview

This project provides a fully interactive trivia game system, featuring both server and client components. The game enables users to participate in a competitive quiz environment over a network, answering timed trivia questions and competing against other players.

## Features

- **Automatic Server Discovery**: Clients can locate the game server through UDP broadcasting, eliminating the need for manual IP input.
- **Efficient Connection Handling**: Once discovered, clients establish a TCP connection with the server. Each client is managed in a separate thread to ensure smooth gameplay for multiple users simultaneously.
- **Multithreaded Gameplay**: Trivia sessions run in parallel threads, allowing the server to efficiently manage multiple players' responses.
- **Dynamic Port Allocation**: The server selects an available TCP port at startup, reducing the need for manual configuration and preventing conflicts.
- **Real-Time Feedback**: Players receive instant feedback on their answers, creating a responsive and engaging game experience.
- **Scalability**: Leveraging Python’s threading module, the server can efficiently handle an increasing number of players.

## Technologies Used

- **Python**: The entire system, both client and server, is developed in Python.
- **Threading**: Ensures concurrent handling of multiple players.
- **Scapy**: Used for UDP broadcast listening during server discovery.
- **Socket Programming**: Manages network communication between the server and clients.

## Project Structure

- `server.py`: Manages game logic, UDP broadcasts, and TCP connections.
- `client.py`: Connects to the server, receives questions, and sends responses.
- `game_statistics.py`: Tracks and updates game statistics.
- `bot.py`: A client bot that can connect and play automatically.

## Installation & Setup

Ensure Python is installed on your system (tested with Python 3.8).

1. Clone the repository:
   ```bash
   git clone https://github.com/omriarie/Trivia-Client-Server.git
   ```
2. Navigate to the project folder:
   ```bash
   cd trivia-game
   ```
3. No additional dependencies are required beyond Python 3.

## Running the Application

### Starting the Server
Run the following command to start the trivia server and broadcast its presence:
   ```bash
   python server.py
   ```

### Connecting a Client
Launch a client using:
   ```bash
   python client.py
   ```
Ensure the server is running before starting the client.

### Running a Bot Client
To simulate a player using a bot, run:
   ```bash
   python bot.py
   ```
