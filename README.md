# Getting Started with an HPC Cluster Using VS Code

This guide explains how to set up Visual Studio Code (VS Code) to connect to a remote High-Performance Computing (HPC) cluster, navigate files, and use the terminal. This is my preferred way of working, however, there are many other options for connection available. If you have any suggestions for improvement on this guide please email me. ~Arman

## 1. Download and Install VS Code
- Visit [[code.visualstudio.com](https://code.visualstudio.com/)](https://code.visualstudio.com/Download).
- Download the installer for your operating system (Windows, macOS, or Linux).
- Run the installer and follow the prompts to install VS Code.
- Launch VS Code after installation.

## 2. Install the Remote - SSH Extension
- In VS Code, click the **Extensions** icon in the Activity Bar (left sidebar, looks like a square with smaller squares).
- Search for **Remote - SSH** in the Extensions Marketplace.
- Click **Install** on the "Remote - SSH" extension by Microsoft.

## 3. Connect to a Remote HPC Cluster
- Ensure you have SSH access to the HPC cluster (consult your cluster admin for credentials and hostname, e.g., `username@cluster.example.com`).
- Open VS Code and press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS) to open the Command Palette.
- Type and select **Remote-SSH: Connect to Host**.
- Choose **Add New SSH Host** and enter the SSH command (e.g., `ssh username@cluster.example.com`).
- Select a config file (usually `~/.ssh/config`) to save the host details.
- In the Command Palette, select **Remote-SSH: Connect to Host** again, choose your cluster, and authenticate (enter password or use SSH key if set up).
- VS Code will set up a remote session, installing necessary server components on the cluster.

## 4. Open File Explorer to Navigate Files
- Once connected, the VS Code interface shows the remote cluster’s environment.
- Click the **Explorer** icon in the Activity Bar (left sidebar, looks like a file).
- The File Explorer opens, displaying the remote file system (e.g., your home directory on the cluster).
- Click folders to navigate or files to open them in the editor.

## 5. Navigate Directories via Terminal
- In VS Code, open the integrated terminal by pressing `Ctrl+`` (backtick) or selecting **Terminal > New Terminal** from the top menu.
- The terminal opens on the remote cluster (you’ll see your cluster’s prompt, e.g., `username@cluster:~$`).
- Use standard Linux commands to navigate:
  - `ls`: List files and directories.
  - `cd directory_name`: Change to a directory.
  - `cd ..`: Move up one directory.
  - `pwd`: Show current directory path.
- Example: To navigate to a folder named `projects`, type `cd projects` and press Enter.

## Notes
- Ensure your HPC cluster allows SSH connections and you have the necessary permissions.
- If you encounter connection issues, verify your SSH configuration or contact your cluster admin.
- Save your work frequently, as remote connections may occasionally disconnect.

For more details, refer to the [VS Code Remote Development documentation](https://code.visualstudio.com/docs/remote/ssh).
