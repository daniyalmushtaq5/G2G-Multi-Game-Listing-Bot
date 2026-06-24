# G2G Multi-Game Listing Bot

## Overview

G2G Multi-Game Listing Bot is a Python automation tool designed to streamline the management of gaming account listings on G2G.

The bot reads account inventory from Excel spreadsheets, automatically creates marketplace listings, fills game-specific attributes, manages existing offers, and handles listing updates across multiple seller profiles.

Built with Selenium, the system automates repetitive marketplace operations and enables large-scale account listing management with minimal manual effort.

---

## Features

### Automated Listing Creation

* Creates G2G account listings automatically.
* Reads account data directly from Excel files.
* Populates listing information based on game-specific requirements.

### Multi-Game Support

Supports listing automation for a wide range of games, including:

* Valorant
* Counter-Strike 2
* League of Legends
* Overwatch
* Overwatch 2
* Fortnite
* Apex Legends
* Call of Duty
* GTA 5 Online
* Rainbow Six Siege
* Rocket League
* Dota 2
* PUBG Mobile
* Sea of Thieves
* Honkai: Star Rail
* Genshin Impact
* Mobile Legends
* Summoners War
* DayZ
* Hay Day
* One Piece Bounty Rush

### Multi-Profile Management

The bot supports multiple Chrome profiles simultaneously:

* Profile 8
* Profile 9
* Profile 16
* Profile 17
* Profile 18

This allows multiple seller accounts to operate independently.

### Excel-Based Inventory Management

Account information is maintained in Excel spreadsheets:

```text id="v1e6b4"
Profile 8.xlsx
Profile 9.xlsx
Profile 16.xlsx
Profile 17.xlsx
Profile 18.xlsx
```

Each spreadsheet acts as a listing queue and inventory database.

### Automated Offer Management

* Creates new listings.
* Updates existing offers.
* Removes outdated listings.
* Tracks processed entries.
* Prevents duplicate listings.

### Game-Specific Listing Logic

Each supported game has customized logic for:

* Region selection
* Rank selection
* Platform selection
* Account attributes
* Marketplace category mapping

---

## Technology Stack

### Automation

* Python
* Selenium WebDriver

### Data Processing

* Pandas
* OpenPyXL

### Browser Management

* Google Chrome
* Chrome Profiles
* ChromeDriver

---

## Project Structure

```text id="i31drh"
G2G-Valorant-Listing-Bot/
│
├── g2glisterbot2.py
│
├── profile_8.py
├── profile_9.py
├── profile_16.py
├── profile_17.py
├── profile_18.py
│
├── Profile 8.xlsx
├── Profile 9.xlsx
├── Profile 16.xlsx
├── Profile 17.xlsx
├── Profile 18.xlsx
│
├── log_8.txt
├── log_9.txt
├── log_16.txt
├── log_17.txt
├── log_18.txt
│
└── README.md
```

---

## Installation

### Clone Repository

```bash id="yop57f"
git clone https://github.com/your-username/G2G-Multi-Game-Listing-Bot.git
cd G2G-Multi-Game-Listing-Bot
```

### Create Virtual Environment

```bash id="5qj9r8"
python -m venv venv
```

### Activate Environment

**Windows**

```bash id="a4m0he"
venv\Scripts\activate
```

**Linux/macOS**

```bash id="xltz6w"
source venv/bin/activate
```

### Install Dependencies

```bash id="2a7kln"
pip install selenium pandas openpyxl webdriver-manager
```

---

## Configuration

### Chrome Profiles

Configure Chrome user profiles used for G2G seller accounts.

Example:

```text id="eh2uv5"
Profile 8
Profile 9
Profile 16
Profile 17
Profile 18
```

### Inventory Files

Each profile uses its own Excel inventory file.

Example columns:

| Game | Title | Price | Rank | Region | Platform | Done |
| ---- | ----- | ----- | ---- | ------ | -------- | ---- |

The bot reads these records and creates listings automatically.

---

## Usage

Launch a specific seller profile:

```bash id="syl39g"
python profile_8.py
```

Or run multiple seller accounts simultaneously:

```bash id="f7v4hi"
python profile_8.py
python profile_9.py
python profile_16.py
python profile_17.py
python profile_18.py
```

The bot will:

1. Open the associated Chrome profile.
2. Log into G2G.
3. Read available account data.
4. Create or manage listings.
5. Update inventory records.
6. Log execution details.

---

## Workflow

```text id="hzrj2f"
Excel Inventory
       │
       ▼
Read Account Data
       │
       ▼
Launch Chrome Profile
       │
       ▼
Open G2G Seller Dashboard
       │
       ▼
Select Game Category
       │
       ▼
Fill Listing Information
       │
       ▼
Publish Listing
       │
       ▼
Update Inventory Status
```

---

## Logging

Each profile maintains a dedicated log file:

```text id="ok4i4z"
log_8.txt
log_9.txt
log_16.txt
log_17.txt
log_18.txt
```

Logs include:

* Listing creation status
* Errors and exceptions
* Processing history
* Execution timestamps

---

## Use Cases

This project is suitable for:

* Gaming account sellers
* Marketplace automation
* Bulk listing management
* Inventory synchronization
* Digital product operations
* Seller workflow automation

---

## Future Enhancements

* Database integration
* Dashboard interface
* Proxy rotation
* Headless browser mode
* Automated pricing adjustments
* Telegram notifications
* Discord alerts
* Multi-marketplace support

---

## Disclaimer

This project is intended for educational and automation purposes only. Users are responsible for complying with G2G's Terms of Service and all applicable marketplace policies.

---

## Author

**Daniyal Mushtaq**

Python Automation Engineer | Marketplace Automation Specialist | Web Scraping Developer

GitHub: https://github.com/daniyalmushtaq5

---

## License

MIT License

Feel free to use, modify, and distribute this project under the terms of the MIT License.
