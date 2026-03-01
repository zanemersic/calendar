# Calendar (Desktop Calendar App)

A desktop calendar application built with Python and Tkinter. It features a Slovenian graphical user interface, allowing users to navigate through months, schedule events, and receive background desktop notifications.

## Features

* **Interactive UI:** Navigate between months and view the current time and date in real-time.
* **Event Creation:** Select any day to add an event with a custom title, description, and specific time.
* **Event Management:** View all scheduled events in a dedicated window and delete them as needed.
* **Desktop Reminders:** A background process monitors your scheduled events and triggers a system notification when the time arrives.
* **Persistent Storage:** All events are automatically saved to a local JSON file (`events.json`) to persist between sessions.

## Prerequisites

Ensure you have Python 3 installed on your system. This project also relies on an external library for desktop notifications.

## Getting Started

1. **Clone or Download the Repository**
2. **Install Dependencies:**
   Open your terminal in the project directory and install the required notification library:
   ```bash
   pip install plyer
   ```
3. **Run the Application:**
   Start the main graphical interface:
   ```bash
   python main.py
   ```

## Project Structure

* **`main.py`**: The core application file containing the Tkinter GUI, clock updates, and calendar rendering.
* **`add_event.py`**: Handles the form for creating new events, saving the data to JSON, and triggering the background reminder script.
* **`events_list.py`**: Manages the interface for listing all saved events sequentially and provides the logic for event deletion.
* **`reminder.py`**: Runs continuously in the background, checking the current system time against the `events.json` database to issue alerts.
