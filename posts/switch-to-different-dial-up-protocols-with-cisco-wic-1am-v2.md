---
title: Switch to different Dial up protocols with Cisco WIC-1AM-V2
date: 2026-10-17
description: ''
---

## I use a Cisco 2811 for the router

- modemcap entry BELL103:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=B103,0,300,300,300,300
- modemcap entry BELL212:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=B212,0,1200,1200,1200,1200
- modemcap entry V21:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=V21,0,300,300,300,300
- modemcap entry V22:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=V22,0,1200,1200,1200,1200
- modemcap entry V22BIS:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=V22B,0,2400,2400,2400,2400
- modemcap entry V23:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=V23C,0,1200,1200,1200,1200
- modemcap entry V32:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=V32,0,9600,9600,9600,9600
- modemcap entry V32BIS:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1+MS=V32B,0,14400,14400,14400,14400
- modemcap entry V34:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1L3M1%C0+DS44=0,0
- modemcap entry V42BIS:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1L3M1+DS44=0,0
- modemcap entry V44:FD=&F:CD=&C1:DTR=&D2:MSC=S0=1L3M1+DS44=3,0

### **To change each entry:**

**modem autoconfigure type _Protocol_**

#### **Example:**

**modem autoconfigure type V34**
