# Pipven: Simplify Python Virtual Environment and Package Management

**Pipven** is a simple yet powerful script that helps you manage Python virtual environments and install/uninstall packages using `pip`. It aims to streamline package management within your projects by providing an intuitive interface with additional features such as colored output and support for `requirements.txt`.

---

## Key Features

- **User-Friendly Interface** : Uses emojis (`✔` for success and `✖` for errors) and colored text (green for successful commands, red for errors) for clear and visually appealing output.
- **Automatic Virtual Environment Management** : Automatically creates and manages a virtual environment if it doesn't already exist.
- **Support for Requirements Files** : Easily install multiple packages from a `requirements.txt` file.
- **Install/Uninstall Packages** : Install or uninstall individual packages with ease.
- **List Installed Packages** : View all installed packages in the virtual environment.
- **Upgrade Packages** : Upgrade specific packages or all outdated packages.
- **Generate Requirements File** : Freeze installed packages into a `requirements.txt` file for reproducibility.
- **Cross-Platform Compatibility** : Works seamlessly on Unix-like systems (Linux, macOS) and can be adapted for Windows.

---

## Installation

### 1. Download from GitHub

You can download the `pipven` script directly from this GitHub repository:

```
curl -o pipven https://raw.githubusercontent.com/vulnquest58/Pipven/refs/heads/main/pipven
```

> Replace `yourusername` with the actual username of the repository owner.

### 2. Make it Executable

After downloading the script, make it executable:

```
chmod +x pipven
```

### 3. Move to PATH

To use the script globally, move it to a directory in your system's `PATH`:


```
sudo mv pipven /usr/local/bin/
```

Now, you can run `pipven` from anywhere in your terminal.

---

## Usage

### Basic Commands

- **Install Packages from `requirements.txt`:**
    
```
    pipven install -r requirements.txt
```
    
- **Install a Single Package:**
    
```
    pipven install package_name
```
    
- **Remove a Package:**
    
```
    pipven remove package_name
```
    
- **List Installed Packages:**
    
```
    pipven list
```
    
- **Upgrade a Specific Package:**
    
```
    pipven upgrade package_name
```
    
- **Upgrade All Outdated Packages:**
    
```
    pipven upgrade -a
```
    
- **Generate `requirements.txt`:**
    
```
    pipven freeze
```
    
- **Display Help Menu:**
    
```
    pipven help
```
Example output:

```
Usage: pipven [options] <action> [args]

Options:
  -v, --venv      Specify the virtual environment directory (default: ./venv)

Actions:
  install         Install a package or packages from a requirements file
  remove          Uninstall a package
  list            List installed packages
  upgrade         Upgrade a package or all packages
  freeze          Generate a requirements.txt file
  help            Display this help message
```

####  **Cross-Platform Compatibility**

- Ensure the script works on both Unix-like systems (Linux, macOS) and Windows by using platform-independent commands or providing separate scripts for Windows.

####  **Python Version Detection**

- Check the Python version before creating the virtual environment to ensure compatibility:
    
```
    python3 --version | grep -q "Python 3" || { error "Python 3 is required."; exit 1; }
```
---

## Options

- `-v`, `--venv`: Specify the virtual environment directory (default: `./venv`).

---

## Example Workflow

4. **Create a Virtual Environment and Install Dependencies:**
    
```
    pipven install -r requirements.txt
```
    
5. **Add a New Package:**
    
```
    pipven install requests
```
    
6. **Upgrade All Packages:**
    
```
    pipven upgrade -a
```
    
7. **Generate Updated `requirements.txt`:**
    
```
    pipven freeze > requirements.txt
```
    
8. **Deactivate the Virtual Environment After Use:** The script automatically deactivates the virtual environment after completing its tasks.
    

---

## Requirements

- **Python 3.x** : Ensure Python 3 is installed on your system.
- **pip** : Python's package installer should be available.

---

## Contributing

Contributions are welcome! If you find any bugs or have suggestions for improvements, please open an issue or submit a pull request.

---

## License

This project is licensed under the [MIT License](https://github.com/vulnquest58/Pipven/blob/main/LICENSE) . Feel free to use, modify, and distribute it as needed.

---

## Acknowledgments

- Thanks to the Python community for creating tools like `venv` and `pip` that make package management easier.
- Special thanks to contributors who help improve this script over time.

---

This `README.md` provides a comprehensive overview of the script's functionality, usage, and key features, making it easy for users to understand and utilize `pipven` effectively.
