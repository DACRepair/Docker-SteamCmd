FROM microsoft/windowsservercore

#Set Default Shell Vars
RUN @echo off

# Set Working Directory
WORKDIR "app\\"

# Setup SteamCMD
ADD https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip steamcmd.zip
RUN echo Expand-Archive -Path "steamcmd.zip" -DestinationPath "." >> temp.ps1
RUN powershell -executionpolicy bypass -File temp.ps1
RUN del steamcmd.zip temp.ps
RUN (steamcmd.exe +quit) ^& exit 0

CMD ['powershell']