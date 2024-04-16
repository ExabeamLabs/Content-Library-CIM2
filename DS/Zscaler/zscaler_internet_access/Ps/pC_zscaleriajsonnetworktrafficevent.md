#### Parser Content
```Java
{
Name = "zscaler-ia-json-network-traffic-event"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Internet Access"
  TimeFormat = ["MMM dd HH:mm:ss yyyy","MMM  dd HH:mm:ss yyyy"]
  ExtractionType = json
  Conditions = [
""""department":"""
""""avgduration":"""
""""locationname":"""
""""event" :{"""
  ]
  Fields = [
    """exa_json_path=$.event.datetime,exa_regex=({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
    """exa_json_path=$.event.action,exa_field_name=result""",
    """exa_json_path=$.event.user,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.event.csip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event.sdip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.event.sdport,exa_field_name=dest_port""",
    """exa_json_path=$.event.csport,exa_field_name=src_port""",
    """exa_json_path=$.event.proto,exa_field_name=protocol""",
    """exa_json_path=$.event.inbytes,exa_field_name=bytes_in""",
    """exa_json_path=$.event.outbytes,exa_field_name=bytes_out""",
    """exa_json_path=$.event.devicehostname,exa_regex=^({host}[\w.-]+)$"""
  ]
  DupFields = [ "result->action" ]


}
```