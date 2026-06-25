# cflt-aiday-2026-outageiq-team-tetris
OutageIQ - Telecom alarm classification solution using AI

## OutageIQ

An AI-based alarm classification and Outage prediction for the Telecom Industry. 

The Network Operations Center (NOC) of any telecom provider gets thousands of alarms per day from telecom network devices like routers, base stations and fibre nodes. Only a portion of these alarms are critical and can lead to a critical outage. However, the NOC team is drowned in the sheer volume of alarms.

![NOC Alarms](images/noc_alarms.png)

## Low-priority Alarms

There are several low-priority and invalid alarms like - 

1. Flapping Alarms (High Frequency + State toggling) - An interface or port keeps going down and coming back up instantly. We see 20 Raised and 20 Cleared alarms from the same card in 1 minute.
2. The Duplicate Alarm / Alarm Storm (High Frequency + Identical State) - A router card fails and sends the same "Power Supply Failed" alarm 500 times in 10 seconds. This drowns the dashboards.
3. Transient Noise (High Frequency + Instant Auto-Clear) - A single faulty event that appears for a split second and vanishes.
4. Symptom Alarms - A single fibre node failing can cause 100 routers downstream to report "Link Down" alarms. These are symptoms, not the root cause.

![Low Priority Alarms](images/low_priority_alarms.png)

## Consequence of Low-Priority Alarms

These "noisy" alarms create several problems -

1. They drown the critical alarms - NOC engineers end up chasing "flapping" links while the core router remains unattended.
2. They cause alert fatigue - Engineers start ignoring alarms, increasing the risk of missing real outages.
3. They impact automation - Auto-ticketing systems create duplicate tickets or noise, wasting NOC bandwidth.