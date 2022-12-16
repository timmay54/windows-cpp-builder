# escape=`
ARG IMAGE_TAG=mcr.microsoft.com/windows/servercore/insider:10.0.20348.1

FROM mcr.microsoft.com/windows/servercore:$IMAGE_TAG

ENV chocolateyUseWindowsCompression=false

RUN ["powershell.exe", "Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))"]
RUN choco install -y powershell-core curl git 
RUN choco install -y visualstudio2017buildtools visualstudio2017-workload-vctools

