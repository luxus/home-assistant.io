---
layout: page
title: "Worldclock"
description: "Instructions how to integrate a Worldclock within Home Assistant."
date: 2015-10-02 11:15
sidebar: true
comments: false
sharing: true
footer: true
logo: home-assistant.png
ha_category: Sensor
ha_iot_class: "Local Push"
---


The `worldclock` sensor platform simple displays the current time in a different time zone

To enable this sensor in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
sensor:
  platform: worldclock
  time_zone: America/New_York
  name: New York
```

Configuration variables:

- **time_zone** (*Required*): The resource or endpoint that contains the value.
- **name** (*Optional*): The name of the sensor, eg. the city.

For valid time zones check the **TZ** column in the [Wikipedia overview](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). Or get the full list from the [pytz](https://pypi.python.org/pypi/pytz) module.

```python
python3 -c "import pytz;print(pytz.all_timezones)"
```
