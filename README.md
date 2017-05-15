## TeamCity Docker agent for Android with emulator
TeamCity Docker agent for building Android app.

### Description

Based on official TeamCity's Build Agent image https://hub.docker.com/r/jetbrains/teamcity-agent/. Involves prerequisites for building Android App including emulator for UI tests. The level of Android API is set to version 25.


### Base Docker Image
[jetbrains/teamcity-agent](https://hub.docker.com/r/jetbrains/teamcity-agent/)


### Installation

1. Install [Docker](https://www.docker.com).
2. Build Android agent image using command:

```
docker build -t teamcity-docker-agent-android:0.1 .
```

### Usage

1. Run TeamCity server with command:
```
docker-compose up server
```
2. Set environment variable URL to IP address of machine where the server is running (for Unix based systems `export URL=ip_address:port`, e.g. `export URL=192.168.0.1:8111`).
3. Run TeamCity agent with command:
```
docker-compose up agent
```
4. [Set up agent for building Android app](https://github.com/mlamojove/teamcity-docker-agent-android/wiki/Teamcity-setup)
