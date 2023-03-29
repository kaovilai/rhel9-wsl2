# Import and Run RHEL9 Distro on WSL2

## Prerequisites

- Windows 10 Professional version 2004 or later
- WSL2
- Docker installed on WSL2 distro

## Importing the Distro

1. Download the exported container `rhel9.tar.gz` from the [latest GitHub release](https://github.com/yourusername/yourrepository/releases).

2. Extract the downloaded `rhel9.tar.gz` file to a directory in your Windows filesystem (e.g., `C:\wslsources`).

3. Open a PowerShell prompt and run the following commands:

```powershell
mkdir c:\wsldistros
cd c:\wsldistros
wsl --import rhel9 ./rhel9 c:\wslsources\rhel9.tar.gz
```

# Running the Distro
1. Launch the new RHEL9 distro:
    ```powershell
    wsl -d rhel9
    ```
2. Check the installed version:
    ```bash
    cat /etc/os-release
    ```
