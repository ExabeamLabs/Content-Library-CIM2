#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-network-traffic-success-networkreceiveaccept
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"event_simpleName":"NetworkReceiveAcceptIP4"""" , """"aip":""", """aid":""" ]
  Fields =[
    """exa_json_path=$.OciContainerId,exa_field_name=container_id"""
    """exa_json_path=$.aip,exa_field_name=aip"""
    """exa_json_path=$.aid,exa_field_name=aid"""
    """exa_json_path=$.cid,exa_field_name=cid"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.ContextProcessId,exa_field_name=process_id"""
    """exa_json_path=$.event_platform,exa_field_name=os"""
    """exa_json_path=$.event_simpleName,exa_field_name=event_name"""
    """exa_json_path=$.name,exa_field_name=process_name"""
    """exa_json_path=$.RemoteAddressIP4,exa_field_name=dest_ip"""
    """exa_json_path=$.LocalAddressIP4,exa_field_name=src_ip"""
    """exa_json_path=$.LocalPort,exa_field_name=src_port"""
    """exa_json_path=$.RemotePort,exa_field_name=dest_port"""
    """exa_json_path=$.ConnectionDirection,exa_field_name=direction"""
  ]


}
```