# EMV-BOT-V1
HOW to install 

git clone https://github.com/evilsaad0-hash/EMV-BOT-V1.git

cd EMV-BOT-V1

apt install unzip 

cd EVM-Bot-V1

sudo bash install.sh

nano .env 

.venv/bin/python bot.py

# 24/7 cmd 

sudo nano /etc/systemd/system/evm-bot.service

[Unit]
Description=EVM Bot V1
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
WorkingDirectory=/root/EVM-Bot-V1
ExecStart=/root/EVM-Bot-V1/.venv/bin/python /root/EVM-Bot-V1/bot.py
Restart=always
RestartSec=5
User=root
Environment=PYTHONUNBUFFERED=1

[Install]
WantedBy=multi-user.target


sudo systemctl daemon-reload
sudo systemctl enable --now evm-bot
sudo systemctl status evm-bot
sudo systemctl restart evm-bot
