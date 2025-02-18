#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-incidentsummaryevent
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """IncidentSummaryEvent""" ]
  Fields = [
    """"eventCreationTime":({time}\d{10})""",
    """"eventType":"({event_category}[^"]+)"""",
    """"IncidentEndTime":({time}\d{10})""",
    """"IncidentStartTime":({time}\d{10})""",
    """"FalconHostLink":"({link}[^"]+)"""",
    """"FineScore":({priority}[.\d]+)""",
    """suid=({user_id}\S+)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"State":"({result}[^"]+)""",
    """"HostID":"({aid}[^"]+)"""",
    """"event_platform":"({os}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
    """"customerIDString":"({cid}[^"]+)""""
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..customerIDString,exa_field_name=cid""",
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_json_path=$.metadata.eventType,exa_field_name=event_category""",
    """exa_json_path=$..IncidentEndTime,exa_field_name=time""",
    """exa_json_path=$..IncidentStartTime,exa_field_name=time"""
    """exa_json_path=$..FalconHostLink,exa_field_name=link"""
    """exa_json_path=$..FineScore,exa_field_name=priority"""
    """exa_json_path=$..State,exa_field_name=result"""
    """exa_json_path=$..HostID,exa_field_name=aid"""
    """exa_json_path=$..event_platform,exa_field_name=os"""
    """exa_json_path=$..cid,exa_field_name=cid"""
        ]


}
```