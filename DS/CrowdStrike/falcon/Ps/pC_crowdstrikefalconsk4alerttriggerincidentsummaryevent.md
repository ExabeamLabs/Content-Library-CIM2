#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-incidentsummaryevent
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """IncidentSummaryEvent""" ]
  Fields = [
    """"eventCreationTime":({time}\d{10})""",
    """"eventType":"({event_category}[^"]+)"""",
    """"IncidentEndTime":({time}\d{10})""",
    """"IncidentStartTime":({time}\d{10})""",
    """"FalconHostLink":"({link}[^"]+)"""",
    """"FineScore":({priority}[.\d]+)""",
    """suid=({user_id}\S+)""",
    """suser=({user}\S+)""",
    """"State":"({result}[^"]+)""",
    """"HostID":"({aid}[^"]+)"""",
    """"event_platform":"({os}[^"]+)""""
        ]


}
```