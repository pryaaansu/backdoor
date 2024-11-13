# Virus and Backdoor Setup for Ethical Hacking

**DISCLAIMER**  
This project is strictly for educational and ethical hacking purposes. Unauthorized use on any machine is illegal and unethical. Ensure you have explicit permission before deploying this tool in any environment.

---

## Overview

This project contains two main components for understanding the mechanisms of remote access tools in a secure, controlled environment:

1. **virus.py**: A backdoor script that, when executed on a target machine, establishes a controlled connection to a server. This allows for remote access and monitoring under explicit permissions.
2. **server.py**: A command-and-control (C2) server script that listens for connections from the backdoor (virus.py), enabling secure, authorized remote control.

This project aims to help ethical hackers and cybersecurity students learn about backdoor mechanisms, remote command execution, and network security testing in authorized setups only.

---

## Components

### 1. `virus.py`

The `virus.py` script acts as a backdoor, designed to be executed on a target machine under a controlled testing environment. When activated, it connects to the server, granting limited remote access capabilities for ethical and authorized use only.

#### Execution

- **Linux**: Execute `virus.py` by navigating to the backdoor directory and running the file.
  ```bash
  cd backdoor
  python3 virus.py
  ```
- **Windows**: To create an executable for Windows, use `pyinstaller` to package `virus.py` into a standalone `.exe` file. This command creates a discreet `.exe` file without a console window, simplifying deployment for authorized testing purposes.
  ```bash
  cd backdoor
  pyinstaller virus.py --onefile --noconsole
  ```

---

### 2. `server.py`

The `server.py` file acts as the C2 server for the `virus.py` backdoor. Running on a secure server, it listens for connections and interacts with connected clients (backdoors), allowing for command execution on remote systems.

#### Execution

- **Linux**: Run the server on a Linux system to ensure compatibility and stability. The server waits for incoming connections and, upon connection, enables controlled interaction with connected clients. Commands entered on the server are executed on the client, and the responses are sent back for review.
  ```bash
  cd backdoor
  python3 server.py
  ```

---

## Important Notes

- **Purpose**: This project is designed solely for educational and ethical hacking purposes. It provides a learning platform for secure backdoor connections and remote command execution in authorized settings.
- **Responsibility**: Use `virus.py` only on machines where you have explicit permission for security testing. Unauthorized access is illegal and punishable under various laws.
- **Testing Environment**: Test this setup in a secure, isolated environment, such as a virtual machine (VM) or an isolated network.

---

## Legal and Ethical Disclaimer

This project is for educational purposes only. Unauthorized deployment or misuse of backdoor programs is illegal and can lead to severe legal consequences. Always follow ethical guidelines and legal standards in cybersecurity practices.

---

## Getting Started

### Prerequisites

Ensure Python 3 is installed on both the server and client machines. To package `virus.py` as an `.exe` file on Windows, `pyinstaller` is required.

### Setup Instructions

1. **Download the Repository**: Clone the repository to your local machine.
   ```bash
   git clone https://github.com/pryaaansu/backdoor
   ```

3. **Start the Server**: Begin by running `server.py` on a server machine.

4. **Deploy the Backdoor**: On the client machine, execute `virus.py` to establish a connection to the server.

   Alternatively, package `virus.py` for Windows as shown in the Components section.

### Command Execution

After a successful connection, enter commands on the server to interact with the client. Responses will be sent back to the server for monitoring and review.

---

## Contributing

If you’re interested in improving this project or adding features, feel free to create a pull request. Always adhere to ethical guidelines and legal standards in any contributions related to cybersecurity.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

**Ethical Usage Only**  
This project should only be used in environments where you have explicit permission for security testing and research purposes.
