#### Parser Content
```Java
{
Name = "zscaler-pa-json-network-traffic-url"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Private Access"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  ExtractionType = json
  Conditions = [ """"Protocol":"HTTP""", """"URL":""", """"Method":""", """"StatusCode":""", """"Customer":"""]
  Fields = [
    """exa_json_path=$.LogTimestamp,exa_field_name=time""",
    """exa_json_path=$.Method,exa_field_name=method""",
    """exa_regex=({protocol}HTTP(S)?)"""
    """exa_json_path=$.URL,exa_field_name=url""",
    """exa_json_path=$.UserAgent,exa_field_name=user_agent,exa_match_expr=!InList($.UserAgent,"")""",
    """exa_json_path=$.RequestSize,exa_field_name=bytes_out""",
    """exa_json_path=$.ResponseSize,exa_field_name=bytes_in""",
    """exa_json_path=$.NameID,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
    """exa_json_path=$.StatusCode,exa_field_name=http_response_code""",
    """exa_json_path=$.ClientPublicIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.ClientPublicPort,exa_field_name=src_port""",
    """exa_json_path=$.ClientPrivateIp,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.ApplicationPort,exa_field_name=dest_port""",
    """exa_json_path=$.ConnectionStatus,exa_field_name=result,exa_match_expr=!InList($.ConnectionStatus,"")""",
    """exa_json_path=$.ConnectionReason,exa_field_name=failure_reason,exa_match_expr=!InList(toLower($.ConnectionReason),"")"""
  ]


}
```