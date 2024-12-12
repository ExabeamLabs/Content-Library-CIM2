#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-activity-scriptcontrolscaninfo"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = "epoch"
Conditions = [
""""event_simpleName":"ScriptControlScanInfo""""
]
Fields = [
""""timestamp":"({time}\d{13})"""",
""""event_simpleName":"({event_code}[^"]+)"""",
""""aid":"({aid}[^"]+)"""",
""""cid":"({cid}[^"]+)"""",
""""event_platform":"({os}[^"]+)"""",
""""ConfigStateHash":"({old_hash}[^"]+)"""",
""""ContextProcessId":"({process_id}[^"]+)"""",
""""aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
""""name":"({event_name}[^"]+)"""",
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$.aid,exa_field_name=aid""",
"""exa_json_path=$.cid,exa_field_name=cid""",
"""exa_json_path=$.event_platform,exa_field_name=os""",
"""exa_json_path=$.ConfigStateHash,exa_field_name=old_hash""",
"""exa_json_path=$.ContextProcessId,exa_field_name=process_id""",
"""exa_json_path=$.aip,exa_regex=({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.name,exa_field_name=event_name""",
"""exa_json_path=$.ScriptContentName,exa_field_name=command_invocation"""
"""exa_json_path=$.ScriptContent,exa_field_name=scriptblock_text"""
]
ParserVersion = "v1.0.0"


}
```