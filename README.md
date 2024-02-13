# ZERO-DAY ZONE Net Tool (Zonecat)

## Overview
Zonecat is a simple command-and-control tool for remote administration of systems over a network. It allows you to listen for incoming connections, execute commands on connected machines, upload files, and interact with a remote shell.

## Usage
Usage: Zonecat.py -t target_host -p port
- -l --listen Listen on [host]:[port] for incoming connections
- -e --execute=file Execute the given file upon receiving a connection
- -c --command Initialize a command shell
- -u --upload=destination Upon receiving connection, upload a file and write to [destination]

## Examples:
```bash
Zonecat.py -t 192.168.0.1 -p 5555 -l -c
```
```bash
Zonecat.py -t 192.168.0.1 -p 5555 -l -u=c:\target.exe
```
```bash
Zonecat.py -t 192.168.0.1 -p 5555 -l -e="cat /etc/passwd"
```
```bash
echo 'ABCDEFGHI' | ./Zonecat.py -t 192.168.11.12 -p 135
```

## Features
- **Listen for Incoming Connections**: Set up a server to listen for incoming connections from remote clients.
- **Execute Commands**: Execute commands on connected machines and receive the output.
- **Upload Files**: Upload files to connected machines.
- **Command Shell**: Interact with a command shell on connected machines.

## Installation
1. Clone the repository:

```bash
git clone https://github.com/Trojanhax/Zonecat.git
```
2. Navigate to the directory:

```bash
cd Zonecat
```
3. Run the script:
```bash
python Zonecat.py [options]
```

## Requirements
- Python 3.x

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
