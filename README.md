# Use-of-the-Firewall

# 1. Enable UFW (if not already enabled)
sudo ufw enable

# 2. List current firewall rules
sudo ufw status verbose

# 3. Block inbound traffic on port 23 (Telnet)
sudo ufw deny 23

# 4. Test the rule (install Telnet if needed)
sudo apt install telnet        # Optional: only if Telnet isn't installed
telnet localhost 23

# 5. Allow SSH (port 22)
sudo ufw allow 22

# 6. Remove the Telnet block rule
sudo ufw delete deny 23
