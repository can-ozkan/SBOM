# Dotnet Installation on Ubuntu
wget https://packages.microsoft.com/config/ubuntu/22.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb \
sudo dpkg -i packages-microsoft-prod.deb \
rm packages-microsoft-prod.deb \
sudo apt update \
sudo apt install dotnet-sdk-8.0 -y
