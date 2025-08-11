#### Parser Content
```Java
{
Name = cloudflare-waf-json-network-traffic-action
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json  
  Conditions = [ """"AccountID":"""", """"Action":"""", """"DestinationIP":"""" , """"Transport":""""]
  Fields = [
    """exa_json_path=$.AccountID,exa_field_name=account_id""",
    """exa_json_path=$.Action,exa_field_name=operation""",
    """exa_json_path=$.Datetime,exa_field_name=time""",
    """exa_json_path=$.DestinationIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.DestinationPort,exa_field_name=dest_port""",
    """exa_json_path=$.SourceIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.DeviceID,exa_field_name=device_id""",
    """exa_json_path=$.DeviceName,exa_field_name=host""",
    """exa_json_path=$.Email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.SessionID,exa_field_name=session_id""",
    """exa_json_path=$.Transport,exa_field_name=protocol""",
    """exa_json_path=$.UserID,exa_field_name=user_id"""
 ]


}
```