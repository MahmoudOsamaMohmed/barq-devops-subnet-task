
Subnet Analyzer

This is a Python-based subnet analysis tool that processes IP address data from an Excel file and calculates:

- CIDR notation
- Network and broadcast addresses
- Number of usable hosts
- Overlapping subnets

__________________________________

Folder Structure

 subnet_analyzer.py       # Main script
 ip_data.xlsx             # Input data (Excel file)
 requirements.txt         # Python dependencies
 Dockerfile               # Docker container definition
 README.md                # This file


__________________________________

How to Run Locally

1. Install dependencies:


pip install -r requirements.txt


2. Run the script:

python subnet_analyzer.py



___________________________________

How to Run with Docker

1. Build the Docker image:


docker build -t subnet-analyzer .

Or with Podman:

podman build -t subnet-analyzer .


2. Run the container:

docker run --rm -v $(pwd):/app subnet-analyzer

Or with Podman:

podman run --rm -v $(pwd):/app subnet-analyzer


____________________________________

Output

The script:

- CSV file "subnet_report_1.csv" show the result of calculation
- CSV file "subnet_report_2.csv" gives some statistics about the data
- barchart "Subnet hosts.png" show the number of hosts in each subnet


____________________________________

Notes

- Make sure your Excel file (`ip_data.xlsx`) has the correct format (2 columns: IP and Subnet Mask) and in the same directory as the script.


