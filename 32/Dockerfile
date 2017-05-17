FROM debian:stretch-slim

RUN dpkg --add-architecture i386 \
	&& apt-get update \
	&& apt-get install -y \
		wine32 \
		wine \
		fonts-wine \
	&& rm -rf /var/lib/apt/lists/*

RUN wineboot
