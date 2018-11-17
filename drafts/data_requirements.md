# Data Requirements Draft

- User data
  - User ID *(Unique)*
  - User Name *(Unique)*
  - User Password
  - User Privilege Level
- Event stream data for Web UI (see JSON at end of file, might be useful for defining MongoDB schema)
  - Datetime: both types have this
  - 2 types of events: one is notification (warning etc.), one is actual data point
    - `notification`
      - `severity_level`
      - `content`
    - `data_point`
      - `mac_src`
      - `mac_dest`
      - `event_type` (say protocol, layer X or stuff, I failed my Rechnernetze LOL so)
      - `packets_count` (Not sure about this one though, is every packet gonna have its own event? If so then this is not needed)
- Raw sensor event stream data to get buffered at Kafka
  - Datetime the event occurs
  - The raw network packets that we will receive from Ankush

Behold.

Notifications will be delivered like this... (Since we pull everything from MongoDB, there will be no live/replay differences here - can be determined by time stamp)

```json
{
  "time_stamp": "2018-11-16T20:50:56.320+01:00",
  "type": "notification",
  "payload": {
    "severity_level": "high",
    "content": "Delayed response from 192.168.1.11 to 192.168.1.10; 13.000ms"
  }
}
```
Data points will be like this.

```json
{
  "time_stamp": "2018-11-16T20:50:56.320+01:00",
  "type": "data_point",
  "payload": {
    "mac_src": "FF:FF:FF:FF:FF:FF",
    "mac_dest": "00:00:00:00:00:00",
    "event_type": "SOME_TYPE",
    "packets_count": 42
  }
}
```

Any thoughts? :D
