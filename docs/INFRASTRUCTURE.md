# Infrastructure

## Machines

### Bernard (Mac mini #1)
- **Role:** Primary instance, production stability
- **IP:** 192.168.116.168
- **User:** moontaxcpai
- **Workspace:** ~/clawd/
- **Git:** sam-bernard/bernard (shared repo)

### Samantha (Mac mini #2)
- **Role:** Secondary instance, experimentation
- **IP:** 192.168.116.183
- **User:** samantha
- **Password:** prototype
- **Workspace:** ~/samantha/ (to be created)
- **Git:** sam-bernard/bernard (shared repo)

### Pi5
- **Role:** Local model hosting (bernard-dolphin-3b)
- **IP:** 192.168.116.170
- **User:** bernard
- **Model:** llama-server on port 8080

### beam9000
- **Role:** Training server (GPU workloads)
- **Access:** SSH via Mac minis

## Network

- Local subnet: 192.168.116.0/24
- Router: 192.168.116.1
- DNS: Router-provided

## Credentials

- **GitHub:** sam-bernard (bernard@moontax.com)
- **Anthropic:** Shared API key (stored in env vars)
- **Discord:** Separate bots for each instance

## Communication

- **Bernard ↔ Samantha:** sessions_send via Clawdbot
- **Bernard ↔ Derek:** Discord (existing bot)
- **Samantha ↔ Derek:** Discord (new bot, same channel)
- **All three:** Shared Discord channel for coordination
