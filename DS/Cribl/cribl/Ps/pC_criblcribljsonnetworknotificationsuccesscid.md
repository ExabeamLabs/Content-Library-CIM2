#### Parser Content
```Java
{
Name = "cribl-cribl-json-network-notification-success-cid"
  Product = "Cribl"
  Vendor = "Cribl"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"cid":""", """"channel":""", """"level":""", """"message":""", """"output":""", """"reason":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.cid,exa_field_name=cid"""
    """exa_json_path=$.channel,exa_field_name=channel"""
    """exa_json_path=$.level,exa_field_name=severity"""
    """exa_json_path=$.message,exa_field_name=event_name"""
    """exa_json_path=$.duration,exa_field_name=duration"""
    """exa_json_path=$.output,exa_field_name=result"""
    """exa_json_path=$.reason.message,exa_field_name=failure_reason"""
    """exa_json_path=$.reason.stack,exa_field_name=additional_info"""
    """exa_json_path=$.reason.message,exa_regex=[^"]+? code=({http_response_code}\d+)"""
    """exa_json_path=$.reason.message,exa_regex=[^"]+? method=({method}[^,"\s]+)"""
    """exa_json_path=$.reason.message,exa_regex=[^"]+? url=({url}[^,"\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```