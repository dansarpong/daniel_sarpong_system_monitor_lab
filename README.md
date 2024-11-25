# System Monitor Lab

This project provides a basic system monitoring script that checks CPU, RAM, and disk usage thresholds and sends email alerts when these thresholds are breached.

## Features

- Monitors system resources:
  - **CPU Usage** (threshold: 2%)
  - **RAM Usage** (threshold: 10%)
  - **Disk Free Space** (threshold: 50%)
- Sends email alerts using the Mailjet API.

## Prerequisites

- Python 3.x
- Install required libraries:
  ```bash
  pip install psutil mailjet-rest
  ```
- Set the following environment variables:
  - `MJ_APIKEY_PUBLIC`: Your Mailjet public API key.
  - `MJ_APIKEY_PRIVATE`: Your Mailjet private API key.
  - `WORK_EMAIL`: The sender email address.
  - `PERSONAL_EMAIL`: The recipient email address.

## How It Works

1. The script collects system metrics (CPU, RAM, and disk usage).
2. If any metric breaches the defined thresholds, an alert email is sent.
3. The email contains the details of the threshold breaches.

## Usage

Run the script directly:
```bash
python3 monitor.py
```
