# Hello World Jenkins Job

## Project Overview

This project demonstrates how to create and run a simple Jenkins Freestyle job that executes a shell script stored in a GitHub repository.

The goal is to understand the basic CI workflow using Git, GitHub, Jenkins, and shell scripting.

## Technologies Used

- Git and GitHub
- Jenkins
- Docker Desktop
- Visual Studio Code
- Bash Shell Scripting

## Project Structure

```text
devops-sample-code/
├── hello-world.sh
└── README.md
```

## Shell Script

The `hello-world.sh` script contains the following code:

```bash
#!/bin/bash
echo "Hello, Jenkins!"
```

## Prerequisites

- Git installed on your system
- A GitHub account
- Visual Studio Code
- Jenkins installed and running
- Docker Desktop, if running Jenkins in a container

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/devops-sample-code.git
cd devops-sample-code
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Configure Jenkins

1. Log in to the Jenkins dashboard.
2. Click **New Item**.
3. Enter `HelloWorld` as the job name.
4. Select **Freestyle project** and click **OK**.
5. Under **Source Code Management**, select **Git**.
6. Enter the repository URL:

   `https://github.com/YOUR_USERNAME/devops-sample-code.git`

7. Set the branch specifier to `*/main`.
8. Under **Build Steps**, select **Execute shell**.
9. Add the following command:

   ```bash
   sh hello-world.sh
   ```

10. Click **Save**.

### 3. Run the Jenkins Job

1. Open the `HelloWorld` job.
2. Click **Build Now**.
3. Open the build number from **Build History**.
4. Click **Console Output** to view the results.

## Expected Output

```text
Hello, Jenkins!
Finished: SUCCESS
```

## Learning Outcomes

- Created and managed a Git repository.
- Pushed source code to GitHub using Git commands.
- Configured a Jenkins Freestyle project.
- Retrieved source code from GitHub.
- Executed a shell script through Jenkins.
- Verified build results using the Jenkins Console Output.

## Future Improvements

- Configure automatic builds using GitHub webhooks.
- Add automated tests to the build process.
- Explore Jenkins Pipeline jobs using a `Jenkinsfile`.

## Author

Created as a beginner DevOps practice project.