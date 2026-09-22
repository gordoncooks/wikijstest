---
title: connecting-a-device
description: 
published: true
date: 2026-09-22T08:57:42.697Z
tags: 
editor: markdown
dateCreated: 2026-09-22T08:54:54.905Z
---

# Connecting a device

Before a device can send readings, it must be registered on the platform and given its credentials.

## 1. Register the device

Go to **Devices → All devices** and click **Add device**. Give it a name and pick the device model. Once saved, copy the device UUID and secret shown on the detail page, the secret is only displayed once.

## 2. Configure the device

Add the credentials to the device's config file:

```yaml
broker: mqtt.mzansisense.co.za
port: 8883
device_uuid: 8f3a21c4-9b77-4e0d-a1f2-6c5d8e9b0011
device_secret: "your-secret-here"
interval: 60
```

## 3. Verify

Restart the device and open **Telemetry → Live data**. Readings should appear within a minute.

If nothing arrives, check that the device has internet access and that the UUID matches the one on the device detail page.