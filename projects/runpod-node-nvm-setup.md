# Installing and Setting Up Node.js and npm in Runpod Jupyter Lab Environment (Using NVM)

This document describes how to set up a Node.js-based web application development environment in a Runpod Jupyter Lab environment. It covers the procedures for installing and managing Node.js and npm using NVM, and concisely summarizes key commands and concepts.

---

## 1. Install NVM (Node Version Manager)

```bash
# Download and execute NVM installation script from GitHub
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

# Activate NVM after installation (restart terminal or run the following commands)
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # This loads nvm bash_completion

# In essence, these commands ensure that NVM is properly configured and its functionalities
# are loaded and accessible within your terminal session, allowing you to use NVM commands.

# Verify installation
nvm --version
2. Install and Use Node.js LTS Version


# Install Node.js 20 LTS version (change '20' if needed)
nvm install 20

# Set Node.js 20 for the current terminal session
nvm use 20

# Set version 20 as default for new terminals as well
nvm alias default 20

# Verify Node.js version
node -v
