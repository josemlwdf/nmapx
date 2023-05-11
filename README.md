# NmapX

NmapX is a bash script that leverages the Nmap command-line tool for network exploration and security auditing. The script performs a port scan on a target IP address or hostname, saves the scan results to a file, and displays the location of the saved file.

## Prerequisites

    Bash: The script is designed to run on a Bash shell environment.
    Nmap: Ensure that Nmap is installed on your system.

## Installation

    Clone the repository or copy the nmapx.sh script to your local machine.
    Open a terminal and navigate to the directory containing the script.
    Run the install.sh script as root using the following command:


``sudo ./install.sh``

This will copy the nmapx.sh script to the system's default executable directory, making it globally accessible.

## Usage

After installing nmapx, you can use it from any directory or location on your system by simply typing nmapx followed by the target IP address or hostname. The script will perform a port scan using Nmap and save the results to a file named nmap.txt in the current directory.


``nmapx <target>``

Replace <target> with the IP address or hostname of the target you want to scan.

## Nmap Parameters

Nmap provides a variety of parameters that allow you to customize the port scanning behavior. The nmapx script supports the following parameters, which you can modify within the script:

    MIN_RATE: Minimum rate of packets sent per second. This controls the speed of the scan. The default value is 5000.
    TIMING: Timing template for the scan. The timing templates range from T0 (paranoid) to T5 (insane). The default value is T4, which provides a balance between scan speed and reliability.
    OPTIONS: Additional Nmap options for the scan. You can specify any valid Nmap options here. The default value is -sCV, which enables service/version detection and default script scanning.

Feel free to modify these parameters in the script to suit your specific scanning requirements.

##Example

``nmapx 192.168.0.1``

This command will perform a port scan on the IP address 192.168.0.1 using the default port scanning options. The results will be saved to a file named nmap.txt in the current directory.

``nmapx -T5 -p1-1024 192.168.0.1``

This command will perform a port scan on the IP address 192.168.0.1 using a timing template of T5 (insane) and scanning ports 1 to 1024. The results will be saved to a file named nmap.txt in the current directory.

## License

This script is licensed under the MIT License. Feel free to use, modify, and distribute it as you please.
