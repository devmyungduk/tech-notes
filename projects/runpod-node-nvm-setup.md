## Introduction

This document explains how to set up a **Node.js-based web application development environment** within a **RunPod Jupyter Lab** instance.  
It provides clear instructions for installing and managing **Node.js** and **npm** using **NVM (Node Version Manager)**, and concisely summarizes the essential commands and concepts needed for development.

RunPod instances run on **Linux (typically Ubuntu)**, so all **bash commands** shown in this guide will work directly in the **JupyterLab terminal**.

> ⚠️ **Note:** These commands will **not work on Windows CMD or PowerShell**.  
> Windows users should use **nvm-windows** instead.

---

## 1. Install NVM (Node Version Manager)

```bash
# Download and execute NVM installation script from GitHub
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

# Activate NVM after installation (restart terminal or run the following commands)
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # This loads nvm bash_completion

# Verify installation
nvm --version

# Install Node.js 20 LTS version (change '20' if needed)
nvm install 20

# Set Node.js 20 for the current terminal session
nvm use 20

# Set version 20 as default for new terminals as well
nvm alias default 20

# Verify both Node.js and npm versions
node -v
npm -v


