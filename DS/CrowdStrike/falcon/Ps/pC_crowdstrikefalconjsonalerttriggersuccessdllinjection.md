#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-dllinjection"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch"
ExtractionType = json
Conditions = [
""""event_simpleName":"DllInjection""""
""""timestamp":""""
]
Fields = [
""""timestamp":\s*"*({time}\d{13})""""
"""\Whostname=(|({host}[^,=]+?)),?(\s+\w+=|\s*\})"""
""""InjectedDll":"({malware_file_name}[^"]+)"""
""""event_simpleName":"({alert_subject}({event_code}({alert_type}({alert_name}[^"]+))))"""
""""id":"({alert_id}[^"]+)"""
""""aid":"({aid}[^"]+)"""
""""cid":"({cid}[^"]+)"""
""""event_platform":"({os}[^"]+)""""
"""exa_json_path=$.raw-event.timestamp,exa_field_name=time""",
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.id,exa_field_name=alert_id""",
"""exa_json_path=$.raw-event.id,exa_field_name=alert_id""",
"""exa_regex=\Whostname=(|({host}[^,=]+?)),?(\s+\w+=|\s*\})"""
"""exa_json_path=$..InjectedDll,exa_field_name=malware_file_name""",
"""exa_json_path=$..event_simpleName,exa_field_name=alert_name""",
"""exa_json_path=$..event_simpleName,exa_field_name=alert_type""",
"""exa_json_path=$..event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$..event_simpleName,exa_field_name=alert_subject""",
"""exa_json_path=$..aid,exa_field_name=aid""",
"""exa_json_path=$..cid,exa_field_name=cid""",
"""exa_json_path=$..event_platform,exa_field_name=os""",
]
ParserVersion = "v1.0.0"


}
```