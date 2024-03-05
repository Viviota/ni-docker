# Get Base Container
# Requires NIPM Based Image
ARG SOURCE_TAG=23.5
FROM viviota/nipm:$SOURCE_TAG

#Define LabVIEW args for path creation
ARG LABVIEW_YEAR=2021
ARG LABVIEW_VERSION=21.1

#Change Working directory to simplify commands
WORKDIR "/Program Files/National Instruments/NI Package Manager"

#Add Feed, Update Feed, and Install
RUN powershell -Command \
    $ErrorActionPreference = 'Stop'; \
	.\nipkg.exe feed-add https://download.ni.com/support/nipkg/products/ni-l/ni-labview-$env:LABVIEW_YEAR-runtime-engine/$env:LABVIEW_VERSION/released --name=ni-labview-runtime-$env:LABVIEW_YEAR ; \
	.\nipkg.exe feed-update; \
	.\nipkg.exe install ni-labview-$env:LABVIEW_YEAR-runtime-engine --accept-eulas --yes --verbose; \
	exit 0

