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

1. **Save the Script** : Save the script as `pipven` in your project directory.
    
2. **Make it Executable** :
    
```
    chmod +x pipven
```
    
3. **Move to PATH** : To use the script globally, move it to a directory in your system's `PATH`:
    
```
    sudo mv pipven /usr/local/bin/
```
    

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
