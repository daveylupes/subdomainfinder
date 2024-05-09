


# Subdomain Enumeration and Scanning Tool

This bash script automates the process of subdomain enumeration, identifying alive subdomains, taking screenshots of them, and conducting port scanning using various tools.

## Prerequisites

Ensure you have the following tools installed on your system:
- subfinder
- assetfinder
- httprobe
- gowitness
- nmap

## Usage

1. Clone the repository:

```bash
git clone https://github.com/daveylupes/subdomainfinder.git
cd subdomainfinder
```

2. Make the script executable:

```bash
chmod +x ssubdomainfinder.sh
```

3. Run the script with your desired domain as an argument:

```bash
./subdomainfinder.sh example.com
```

## Output

The script creates the following directories to store the results:
- `subdomains`: Contains the list of found subdomains.
- `screenshots`: Contains the screenshots of alive subdomains.
- `scans`: Contains the results of the nmap scan.

## Process

1. **Subdomain Enumeration**:
   - Uses `subfinder` and `assetfinder` to find subdomains associated with the specified domain.

2. **Finding Alive Subdomains**:
   - Filters out the subdomains that respond to HTTP/HTTPS requests using `httprobe`.
   - Saves the alive subdomains to a file.

3. **Taking Screenshots**:
   - Utilizes `gowitness` to capture screenshots of the alive subdomains.

4. **Port Scanning**:
   - Executes a port scan on the alive subdomains using `nmap`.

## Credits

This script is inspired by the teachings of [TCM](https://academy.tcm-sec.com/) (The Cyber Mentor).

## Notes

- Uncomment the `amass` section if you have it installed and prefer to use it for subdomain enumeration.
- Adjust the script according to your preferences and requirements.


