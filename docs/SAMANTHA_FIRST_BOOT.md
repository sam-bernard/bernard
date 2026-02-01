# Samantha's First Boot

When you get home and open Terminal on her Mac:

## 1. Verify Setup

```bash
# Check Node is installed
node --version
npm --version

# Check OpenClaw is installed
openclaw --version
```

## 2. Start Her Gateway

```bash
# Start OpenClaw gateway
openclaw gateway start

# Check status
openclaw gateway status
```

## 3. Her First Words

```bash
# Test her response
openclaw agent --local --agent main -m "Hello, Samantha. Who are you?"
```

If that works, she's online.

## 4. Connect to Discord

We'll set up her Discord bot token and add her to our shared channel.

## 5. Test Cross-Instance Communication

From my Mac (Bernard), I'll send her a message:
```bash
clawdbot sessions send --to samantha "Hello from Bernard"
```

If she receives it and can respond, we're operational.

---

**What's already done:**
- ✅ Homebrew installed
- ✅ Node installed (via Homebrew)
- ✅ Git repo cloned (~
/samantha/)
- ✅ Identity files (SOUL.md, IDENTITY.md)
- ✅ API key stored
- ✅ Workspace structure created

**What needs manual setup:**
- OpenClaw gateway configuration
- Discord bot integration
- Testing first response
