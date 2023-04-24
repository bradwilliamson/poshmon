PoshMon

PoshMon is a PowerShell module for monitoring network latency and jitter. It provides real-time statistics on ping response times, packet loss, and jitter to help you analyze the quality of your network connection.
Features

    Monitor ping response times for a target host or IP address
    Real-time statistics on lowest, highest, and average ping response times
    Calculate packet loss percentage
    Calculate jitter and average jitter
    Retrieve your Internet Service Provider (ISP) name
    Calculate the standard deviation of an array of numbers

InfluxDB integration is being worked on and might be available in a future edition. This would allow sending ping monitoring data to InfluxDB for visualization in Grafana.

Monitoring system resources on the local PC is also planned for future development.
Installation

    Clone the repository or download the source code:

bash

git clone https://github.com/yourusername/poshmon.git

    Change to the poshmon directory and import the module:

powershell

cd poshmon
Import-Module .\poshmon.psm1

Usage
Start-PingMonitor

To start monitoring the ping to a target host or IP address, use the Start-PingMonitor function:

powershell

Start-PingMonitor -Target "google.com"

Replace "google.com" with your desired host or IP address.
Get-ISP

This function retrieves your Internet Service Provider (ISP) name by querying your public IP address.

Usage:

powershell

Get-ISP

Get-StandardDeviation

This function calculates the standard deviation of an array of numbers.

Usage:

powershell

$numbers = @(5, 10, 15, 20, 25)
Get-StandardDeviation -Numbers $numbers

Replace @(5, 10, 15, 20, 25) with your desired array of numbers.