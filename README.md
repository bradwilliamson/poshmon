# PoshMon

PoshMon is a PowerShell module which started out as a simple tool for monitoring network latency, packet loss, standard deviation and jitter with ongoing disputes with my current. Internet Service Provider. It provides real-time statistics on response times, packet loss, and jitter to help you analyze the quality of your network connection. It is now being rewritten as a powershell monitoring platform for monitoring all things possible on systems, and network connecitivity. With the end goal of exporting that data into InfluxDB or other data sources for Grafana

## Features

- Monitor ping response times for a target host or IP address
- Real-time statistics on lowest, highest, and average ping response times
- Calculate packet loss percentage
- Calculate jitter and average jitter
- Retrieve your Internet Service Provider (ISP) name
- Calculate the standard deviation of an array of numbers

InfluxDB integration is being worked on and might be available in a future edition. This would allow sending ping monitoring data to InfluxDB for visualization in Grafana.

Monitoring system resources on the local PC is also planned for future development.

## Installation

1. Clone the repository or download the source code:

    ```bash
    git clone https://github.com/yourusername/poshmon.git
    ```

2. Change to the `poshmon` directory and import the module:

    ```powershell
    cd poshmon
    Import-Module .\poshmon.psd1
    ```

## Usage

### Start-PingMonitor

To start monitoring the ping to a target host or IP address, use the `Start-PingMonitor` function:

```powershell
Start-PingMonitor -Target "8.8.8.8"

```powershell
Get-ISP

```powershell
$numbers = @(5, 10, 15, 20, 25)
Get-StandardDeviation -Numbers $numbers
