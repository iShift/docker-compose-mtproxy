# docker-compose-mtproxy
With docker-compose file you can easy install telegram mtproto proxy and configure it.

# Docker
If you have one, read next, if not:

`curl -sSL https://get.docker.com/ | sh`

install docker-compose
On Ubuntu/Debian:

`sudo apt-get update`

`sudo apt-get install docker-compose`

or

`sudo apt-get -y install python-pip`

`sudo pip install docker-compose`


# Clone repository
`git clone https://github.com/iShift/docker-compose-mtproxy.git`

# Edit config.env
In that file you can configure:
- TAG Value, for promote channel
- Preset SECRET, UP TO 16
- Secret count for generate, UP TO 16
- Workers count

# Change proxy port
By default, proxy start at 443 port, if you want another - edit **docker-compose.yml**:
- "**443**:443" 

# Start proxy
go to folder with that repository:

`cd docker-compose-mtproxy`

and run:

`docker-compose up -d`

# Get logs and connections info
`docker-compose logs`


# Stop proxy
From repository folder:

`docker-compose down`

# Error ERROR: Couldn't connect to Docker daemon at http+docker://localhost - is it running?
Use `sudo` with docker comands or add your account to docker group:
`sudo usermod -aG docker $(whoami)`

# Links
Telegram docker hub: https://hub.docker.com/r/telegrammessenger/proxy/

Source Code: https://github.com/TelegramMessenger/MTProxy
