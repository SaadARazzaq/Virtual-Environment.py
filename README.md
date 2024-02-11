# 📦Creating a Virtual Environment in Python

![image](https://github.com/SaadARazzaq/venv.py/assets/123338307/8896dc55-5453-43a6-97ee-df4e3195cae7)

**👉HIGHLY RECOMMEND VS Code FOR THE VIRTUAL ENVIRONMENT SETUP**

A virtual environment is a self-contained Python environment that allows you to isolate and manage your Python dependencies for different projects. This is important when:

- You need to install specific packages for a project, and they may conflict with packages required by other projects.
- You want to share your project with someone else, and you want to ensure they have the exact same environment without worrying about package conflicts or version mismatches.


## 🔗Why Use Virtual Environments?

### Isolation of Dependencies 🔒

In Python, different projects often require different sets of packages and dependencies. Installing all packages globally can lead to conflicts and compatibility issues. Virtual environments provide a solution by allowing you to create isolated environments for each project.

With virtual environments, you can:

- Install project-specific packages without affecting the global Python environment.
- Keep dependencies separate, preventing conflicts between projects.
- Easily switch between different project environments.

### Reproducibility 🚀

Virtual environments help ensure that your project remains reproducible. When you create a virtual environment and list the project's dependencies in a `requirements.txt` file, you can recreate the exact same environment on another machine or for a colleague.

This is especially useful when:

- Sharing your code with others who may not have the same packages installed.
- Collaborating on a project with team members who need consistent development environments.
- Deploying your application to a server with a controlled environment.


## ⚙️Creating Virtual Environments

Here's how to create a virtual environment using the `python -m venv` command:

- **Windows**: Open Command Prompt or PowerShell and run:
```bash
python -m venv myenv
.\myenv\Scripts\Activate
```

- **Linux and macOS**: Open a terminal and run:
```bash
python -m venv myenv
source myenv/bin/activate
```


## 🚪Deactivating the Virtual Environment

To deactivate the virtual environment and return to the global Python environment, run:
```bash
deactivate
```

This will deactivate the virtual environment and restore your Python environment to its default state.


## Issues that might come

<img width="532" alt="image" src="https://github.com/SaadARazzaq/venvpy/assets/123338307/be90c3b6-2b77-40aa-9a4c-05f7f9f49587">

 If this issue comes then this means that you're encountering an issue with PowerShell's execution policy, which is preventing the activation script from running. PowerShell's execution policy is a security feature that controls the conditions under which PowerShell loads configuration files and runs scripts.

To resolve this issue, you can temporarily change the execution policy for the current PowerShell session to allow script execution. Here's how you can do it:

- Open PowerShell as an administrator. Right-click on the PowerShell icon and select "Run as administrator".
- Run the following command to temporarily set the execution policy to allow script execution:

```bash
Set-ExecutionPolicy RemoteSigned -Scope Process
```

- After changing the execution policy, try activating the virtual environment again using the activation script:

```bash
.\myenv\Scripts\Activate
```

This should allow you to activate the virtual environment without encountering the security error. Once you've finished working in the virtual environment, you can close the PowerShell session, and the temporary execution policy change will revert to the previous state.

To permanently set the execution policy for PowerShell, you'll need to run the Set-ExecutionPolicy command with appropriate parameters. Here's how you can do it:

- Open PowerShell as an administrator. Right-click on the PowerShell icon and select "Run as administrator".
- Run the following command to permanently set the execution policy to RemoteSigned for the current user:

```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

This command sets the execution policy to RemoteSigned for the current user only. It allows scripts that are downloaded from the internet to run if they are signed by a trusted publisher.

If you want to set the execution policy for all users on the computer, you can use the AllSigned policy, which requires all scripts to be signed by a trusted publisher. However, this may be more restrictive:

```bash
Set-ExecutionPolicy RemoteSigned -Scope LocalMachine
```

**Be cautious when setting the execution policy, especially to a less restrictive one like RemoteSigned, as it can pose security risks if you run untrusted scripts. Always ensure that you only execute scripts from trusted sources.**

---

Now you know how to create a virtual environment in Python on different operating systems and why it's important. Virtual environments are essential for managing dependencies, ensuring project isolation, and maintaining reproducibility in your Python projects. 😊

```bash
Made with 💖 by Saad
```
