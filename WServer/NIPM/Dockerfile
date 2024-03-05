# Get Base Container
FROM mcr.microsoft.com/windows/server:ltsc2022
ARG NIPM_VERSION=23.5.0

## Create Users
#RUN net accounts /maxpwage:unlimited
#RUN net user Container /add /expire:never /passwordreq:no
#RUN net localgroup Administrators Container /add

##Switch to User
#USER Container

##Download and install NIPM
##RUN echo "%NIPM_VERSION%"
##RUN powershell echo "$env:NIPM_VERSION"
RUN powershell -Command \
	$ProgressPreference = 'SilentlyContinue'; \
    $ErrorActionPreference = 'Stop'; \
	Invoke-WebRequest -Uri https://download.ni.com/support/nipkg/products/ni-package-manager/installers/NIPackageManager$env:NIPM_VERSION.exe -OutFile C:\users\public\downloads\NIPackageManager.exe; \
	Start-Process -FilePath "C:\users\public\downloads\NIPackageManager.exe" -ArgumentList "--passive", "--accept-eulas", "--prevent-reboot" -Wait; \
	Remove-Item C:\users\public\downloads\NIPackageManager.exe -Force

WORKDIR "/Program Files/National Instruments/NI Package Manager"	
RUN nipkg.exe config-set nipkg.enable-NI-connectivity false && \
	nipkg.exe config-set nipkg.cachepackages false
	