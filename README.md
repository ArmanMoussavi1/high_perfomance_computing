# Getting Started with an HPC Cluster Using VS Code

Welcome, Northwestern students! This guide is designed for beginners to help you connect to Northwestern’s **Quest HPC cluster** using **Visual Studio Code (VS Code)**. It covers downloading VS Code, connecting to Quest, navigating files, and using the terminal. If you have suggestions to improve this guide, please email me! ~Arman

Last updated: 10/16/2025

## 1. Download and Install VS Code
VS Code is a free, user-friendly code editor that works on Windows, macOS, or Linux.

1. Go to https://code.visualstudio.com/Download.
2. Download the version for your computer (Windows, macOS, or Linux).
3. Open the downloaded file and follow the simple installation steps.
4. Open VS Code by clicking its icon after installation.

## 2. Install the Remote - SSH Extension
This extension lets you connect VS Code to Quest.

1. Open VS Code.
2. On the left sidebar, click the **Extensions** icon (it looks like a square with smaller squares).
3. In the search bar, type **Remote - SSH**.
4. Find the **Remote - SSH** extension by Microsoft and click **Install**.

## 3. Connect to the Quest HPC Cluster
To connect to Quest, you need your **NetID** and the Quest hostname (`quest.northwestern.edu`). You’ll get these after securing a Quest account (see the **Northwestern Students: Getting a Quest Account** section below).

1. Open VS Code and press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS) to open the **Command Palette**.
2. Type **Remote-SSH: Connect to Host** and select it.
3. Choose **Add New SSH Host**.
4. Enter `ssh yourNetID@quest.northwestern.edu` (replace `yourNetID` with your actual NetID).
5. Select the default config file (usually `~/.ssh/config`) to save the connection.
6. In the Command Palette, select **Remote-SSH: Connect to Host** again and choose `quest.northwestern.edu`.
7. Enter your NetID password when prompted (or set up an SSH key for easier access—ask your instructor or email rcs@northwestern.edu for help).
8. VS Code will connect to Quest and set up a remote session (this may take a minute).

## 4. Navigate Files Using File Explorer
Once connected, you can explore Quest’s files visually in VS Code.

1. On the left sidebar, click the **Explorer** icon (it looks like a file).
2. The **File Explorer** will show your Quest home directory (e.g., `/home/yourNetID`).
3. Click folders to open them or files to view/edit them in VS Code.

## 5. Navigate Directories Using the Terminal
You can also navigate Quest using text commands in the terminal, like a command-line pro!

1. In VS Code, open the terminal by pressing `Ctrl+`` (backtick) or selecting **Terminal > New Terminal** from the top menu.
2. You’ll see a prompt like `yourNetID@quest:~$`, meaning you’re on Quest.
3. Use these basic commands:
   - `ls`: Shows files and folders in your current directory.
   - `cd folder_name`: Moves into a folder (e.g., `cd projects`).
   - `cd ..`: Moves up one folder.
   - `pwd`: Shows your current location on Quest.
4. Example: To enter a folder called `projects`, type `cd projects` and press Enter.

## Notes
- Make sure you have a Quest account (see below) and internet access.
- If you can’t connect, double-check your NetID, password, or contact rcs@northwestern.edu.
- Save your work often, as remote connections can sometimes drop.
- For more help, check the VS Code Remote Development guide: https://code.visualstudio.com/docs/remote/ssh.

## For Northwestern University Students: Getting a Quest Account
**Quest** is Northwestern’s powerful HPC cluster for research and coursework, managed by Research Computing Services. As a student, you usually join an existing allocation through a faculty advisor (for research) or instructor (for classes). Allocations are free but require approval.

### Option 1: Join an Existing Allocation (Easiest for Students)
- **For Research (via Faculty Advisor):**
  1. Talk to your faculty advisor who has an active Quest allocation.
  2. Ask them to add your **NetID** to their allocation using the Add Allocation Participant form: https://www.it.northwestern.edu/secure/forms/research/allocation-request-forms.html.
  3. After approval (1-2 weeks), you’ll get an email with your Quest account details (username: your NetID; hostname: `quest.northwestern.edu`).

- **For Coursework or Workshops (via Instructor):**
  1. Your instructor will add your **NetID** to their class or workshop allocation.
  2. They use the Add Workshop & Classroom Participant form: https://www.it.northwestern.edu/secure/forms/research/allocation-request-forms.html.
  3. Your account lasts for the class duration (note: files may be deleted when the class ends unless you’re part of another allocation).

### Option 2: Apply for a New Allocation (Rare for Students)
This is uncommon for students unless you’re doing an independent project (e.g., honors thesis) without a faculty advisor’s allocation.

1. Fill out the Research Allocation I form: https://www.it.northwestern.edu/secure/forms/research/allocation-request-forms.html.
2. Write a short proposal explaining your project, why you need Quest, and how much computing power you need.
3. Submit by the quarterly deadline (check Allocation Submission Guidelines: https://www.it.northwestern.edu/departments/it-services-support/research/computing/quest/general-access-allocation-types.html).
4. The Allocation Committee reviews your application. If approved, you’ll get a starter allocation (limited computing resources) for one year.

### After Getting Your Quest Account
- Log in using `ssh yourNetID@quest.northwestern.edu` in VS Code or other SSH tools.
- Check the Quest User Guide for tips on setting up SSH keys or transferring files (use Globus for large data): https://services.northwestern.edu/TDClient/30/Portal/KB/ArticleDet?ID=505.
- Email rcs@northwestern.edu for support or to schedule a consultation.

### Important Notes
- Quest cannot process sensitive data (e.g., medical or personal info). Ask your advisor if unsure.
- Make sure your advisor or instructor submits your NetID for access.
- Check Quest’s status at: https://www.it.northwestern.edu/status.

Happy computing! If you’re stuck, reach out to rcs@northwestern.edu or your advisor/instructor. ~Arman
