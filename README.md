# Tennis Court Monitor

A Python application that monitors a tennis court using a webcam and checks for unauthorized usage by comparing court reservations with detected people.

## Features

- Webcam monitoring with YOLOv8 person detection
- Integration with GotCourts reservation system
- Automatic detection of unauthorized court usage
- Regular status updates every 10 minutes

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/tennis-court-monitor.git
cd tennis-court-monitor
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Copy the environment template and fill in your credentials:
```bash
cp .env.example .env
```

5. Edit the `.env` file with your credentials:
- `CLUB_ID`: Your club ID from GotCourts
- `COURT_ID`: Your court ID from GotCourts
- `GOTCOURTS_API_KEY`: Your GotCourts API key
- `GOTCOURTS_PHPSESSID`: Your GotCourts session ID
- `WEBCAM_URL`: URL of your court's webcam

## Usage

Run the monitor:
```bash
python court_monitor.py
```

The script will:
- Check court reservation status every 10 minutes
- Monitor the webcam for people
- Alert if people are detected on a reserved court

## Security Note

Never commit your `.env` file to version control. The `.gitignore` file is configured to prevent this.

## License

MIT License - feel free to use and modify for your needs. 
