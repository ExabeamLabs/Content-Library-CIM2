#### Parser Content
```Java
{
Name = pan-xsoar-json-alert-trigger-success-xsoar
  Vendor = Palo Alto Networks
  Product = Cortex XSOAR
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  ExtractionType = json
  Conditions = [ """"severity":"""", """"snowNumber"""", """"id":"XSOAR""" ]
  Fields = [
    """exa_json_path=$.username,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.type,exa_field_name=alert_type"""
    """exa_json_path=$.platform,exa_field_name=alert_source"""
    """exa_json_path=$.id,exa_field_name=alert_id"""
    """exa_json_path=$.name,exa_field_name=alert_name"""
    """exa_json_path=$.createdOn,exa_field_name=time"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.hostname,exa_regex=^({host}[\w\-.]+)$"""
    """exa_json_path=$.sourceIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```