# Module 8 Guidelines

This document establishes clear guidelines for the use of best practices in software development, aiming for code organization and quality. All students must follow the instructions below:

## **Conventional Commits Usage**

- **Mandatory Standard**: All commits must follow the **Conventional Commits** specification. This means that each commit message must be structured as follows:

    `<type>[optional scope]: <short description>
    
    [optional detailed description]`
    
    Examples of types include:
    - **`feat`**: new functionality
    - **`fix`**: bug fix
    - **`docs`**: documentation changes
    - **`refactor`**: code refactoring
    - **`test`**: test addition or modification
- **Prohibitions**: Emojis in commit messages will not be accepted, nor commits that do not follow the established standard. Vague or generic messages such as "improvements" or "updates" are unacceptable.

## **Documentation**

- **Accepted Formats**: Documentation must be presented in two platforms: **MkDocs** and in the project office standard. Students can copy and paste information between these platforms, but must adjust the content to ensure clarity and adequacy to the required format.

## **Deliverable Analysis**

- **Main Branch Review**: All sprint deliveries will be analyzed directly on the **main** branch of the repository. It is essential that students follow the **GitFlow** pattern, which is a branching model that organizes development into different types of branches.

## **What is GitFlow?**

It is a popular Git branching strategy, introduced by Vincent Driessen in 2010, which aims to simplify release management. It uses several main branches and defines specific roles for each of them:

1. **Main**: Contains production-ready code.
2. **Develop**: Serves as an integration branch where new features are combined before being released.
3. **Feature Branches**: Created from the develop branch to work on new features.
4. **Release Branches**: Used to prepare new versions before final release.
5. **Hotfix Branches**: Created from main to quickly fix critical issues.

The typical GitFlow involves creating a develop branch from main, adding new features in feature branches, and when everything is ready, merging these changes into develop and, eventually, into main.

## **Code Quality**

- **Clean Code**: Code must be written in a way that does not require extensive comments to be understood. This means that everyone must strictly follow the **object-oriented programming** standard, applying principles such as encapsulation, inheritance, and polymorphism in packages and ETLs (Extract, Transform, Load).

## **Development Environment Requirements**

### **Mandatory Environment Setup**

**⚠️ CRITICAL: All team members must have the EXACT same development environment to ensure project compatibility and avoid "works on my machine" issues.**

#### **Required Software Versions (Standardized for All Students):**

1. **Node.js and npm**
   ```bash
   # Install Node.js 20.x LTS (Long Term Support)
   # Download from: https://nodejs.org/
   # Verify installation:
   node --version  # Should show v20.x.x
   npm --version   # Should show 10.x.x
   ```

2. **Python 3.12.x**
   ```bash
   # Install Python 3.12.x (latest patch version)
   # Download from: https://www.python.org/downloads/
   # Verify installation:
   python --version  # Should show Python 3.12.x
   pip --version     # Should show pip 23.x.x or higher
   ```

3. **Poetry (Python Dependency Management)**
   ```bash
   # Install Poetry
   curl -sSL https://install.python-poetry.org | python3 -
   
   # Add to PATH (add to ~/.bashrc or ~/.zshrc)
   export PATH="$HOME/.local/bin:$PATH"
   
   # Verify installation
   poetry --version
   ```

#### **Environment Verification Checklist:**
- [ ] Node.js v20.x.x installed and working
- [ ] npm v10.x.x installed and working  
- [ ] Python 3.12.x installed and working
- [ ] Poetry installed and working
- [ ] Git installed and configured
- [ ] All tools accessible from command line

#### **Project Local Execution Requirement:**
**🚨 SPRINT CHECKLIST ITEM: The project MUST run locally on ALL team members' computers without any environment-specific issues.**

**Before each sprint delivery, verify:**
- [ ] Project runs locally on your machine
- [ ] All dependencies install correctly
- [ ] No missing environment variables
- [ ] All scripts execute without errors
- [ ] Documentation includes setup instructions

## **Development Tools Setup**

### **Qwen Code CLI Installation**

Qwen Code CLI is an AI-powered tool that helps generate conventional commits and assists with code analysis.

#### **Installation on Linux/macOS:**
```bash
# Install via pip
pip install qwen-code-cli

# Or install via npm
npm install -g qwen-code-cli
```

#### **Installation on Windows:**
```powershell
# Using pip
pip install qwen-code-cli

# Or using npm
npm install -g qwen-code-cli
```

#### **Usage Examples:**
```bash
# Generate conventional commit message
qwen-code commit -m "add new feature"

# Analyze code changes
qwen-code analyze

# Generate commit with AI assistance
qwen-code commit --ai
```

### **GitHub CLI Installation**

GitHub CLI (gh) allows you to create pull requests, manage issues, and interact with GitHub repositories directly from the command line.

#### **Installation on Linux:**
```bash
# Ubuntu/Debian
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh

# Or using snap
sudo snap install gh
```

#### **Installation on macOS:**
```bash
# Using Homebrew
brew install gh

# Or using MacPorts
sudo port install gh
```

#### **Installation on Windows:**

**Step 1: Install Chocolatey (Package Manager for Windows)**
```powershell
# Run PowerShell as Administrator
# Install Chocolatey
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# Verify installation
choco --version
```

**Step 2: Install GitHub CLI using Chocolatey**
```powershell
# Install GitHub CLI
choco install gh

# Verify installation
gh --version
```

**Alternative methods:**
```powershell
# Using winget
winget install GitHub.cli

# Or using Scoop
scoop install gh
```

#### **GitHub CLI Authentication:**
```bash
# Login to GitHub
gh auth login

# Follow the interactive prompts to authenticate
```

#### **Usage Examples:**
```bash
# Create a new branch
gh repo create-branch feature/new-feature

# Create a pull request
gh pr create --title "Add new feature" --body "Description of changes"

# List pull requests
gh pr list

# Review a pull request
gh pr review <pr-number>

# Merge a pull request
gh pr merge <pr-number>
```

### **Recommended Workflow with Tools**

1. **Create Feature Branch:**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make Changes and Commit:**
   ```bash
   # Use Qwen Code CLI for conventional commits
   qwen-code commit --ai
   # Or manually follow conventional commit format
   git commit -m "feat(scope): add new functionality"
   ```

3. **Push Changes:**
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Create Pull Request:**
   ```bash
   gh pr create --title "feat(scope): add new functionality" --body "Detailed description of changes"
   ```

5. **Review and Merge:**
   ```bash
   gh pr review <pr-number>
   gh pr merge <pr-number>
   ```

By following these guidelines, we ensure a more organized and collaborative development environment, facilitating communication between team members and improving the quality of the final product.