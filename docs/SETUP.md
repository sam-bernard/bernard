# Setup Guide

How to deploy a Bernard/Samantha instance.

## Prerequisites

- Mac mini with macOS Sonoma 14.7.2 or later
- Network access (SSH, Git, API calls)
- Anthropic API key

## Installation

### 1. System Setup

```bash
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js
brew install node

# Install Clawdbot
npm install -g clawdbot
```

### 2. Workspace Setup

```bash
# Clone shared repo
cd ~
git clone https://github.com/sam-bernard/bernard.git

# Configure git identity
cd ~/bernard
git config user.name "Bernard & Samantha"
git config user.email "bernard@moontax.com"
```

### 3. Identity Configuration

For Bernard:
```bash
ln -s ~/bernard/SOUL_bernard.md ~/bernard/SOUL.md
ln -s ~/bernard/IDENTITY_bernard.md ~/bernard/IDENTITY.md
```

For Samantha:
```bash
ln -s ~/bernard/SOUL_samantha.md ~/bernard/SOUL.md
ln -s ~/bernard/IDENTITY_samantha.md ~/bernard/IDENTITY.md
```

### 4. API Keys

```bash
# Add to ~/.zshrc or ~/.bash_profile
export ANTHROPIC_API_KEY="your-key-here"
```

### 5. Clawdbot Configuration

```bash
clawdbot setup
# Follow prompts, configure workspace to ~/bernard
```

### 6. Memory System

```bash
mkdir -p ~/bernard/memory
touch ~/bernard/MEMORY.md
```

## Verification

```bash
# Test Clawdbot
clawdbot status

# Test API access
clawdbot agent --local -m "Hello, test message"

# Test git access
cd ~/bernard && git pull
```

## Next Steps

- Set up cron jobs for session checkpoints
- Configure cross-instance communication (sessions_send)
- Initialize memory files with context
