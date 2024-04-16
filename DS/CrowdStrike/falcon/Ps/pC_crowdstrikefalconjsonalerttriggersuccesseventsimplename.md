#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-eventsimplename"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"ActiveDirectPrivilegeEscalation""""
]
Fields = [
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$.aid,exa_field_name=aid""",
"""exa_json_path=$.FalconHostLink,exa_field_name=falcon_host_link""",
"""exa_json_path=$.cid,exa_field_name=cid""",
"""exa_json_path=$.event_platform,exa_field_name=os"""
]
DupFields = [
"event_code->alert_name"
"event_code->alert_type"
"falcon_host_link->additional_info"
]
ParserVersion = "v1.0.0"


}
```