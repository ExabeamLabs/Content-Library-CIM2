#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-service-stop-success-hostedservicestopped
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ """"event_simpleName":"HostedServiceStopped"""", """"aip"""", """"aid"""" ]
  Fields = [
    """timestamp":"({time}\d{10,13})"""
    """"event_simpleName":"({event_name}[^"]+)"""",
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"event_platform":"({os}[^"]+)"""",
    """"ServiceDisplayName":"({service_name}[^"]+)"""",
    """"aid":"({aid}[^",]+)""",
    """"cid":"({cid}[^",]+)""",
    """"destinationServiceName":"({app}[^",]+)""",
    """"dproc":"({dproc}[^",]+)""",
    """"TargetProcessId":"({dest_process_id}[^",]+)""",
    """"name":"({event_name}[^",]+)"""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """exa_json_path=$.name,exa_field_name=service_name""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.ServiceDisplayName,exa_field_name=service_name""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.cid,exa_field_name=cid"""
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.dproc,exa_field_name=dproc"""
    """exa_json_path=$.TargetProcessId,exa_field_name=dest_process_id"""
    """exa_json_path=$.name,exa_field_name=event_name"""
  ]


}
```