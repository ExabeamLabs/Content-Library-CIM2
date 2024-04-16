#### Parser Content
```Java
{
Name = microsoft-defenderep-json-user-password-modify-success-passwordchanged
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"category":""", """"AdvancedHunting-IdentityDirectoryEvents"""", """"ActionType":""",""""Account Password changed"""" ]
  Fields = [
    """exa_json_path=$.properties.Timestamp,exa_field_name=time""",
    """exa_json_path=$.properties.TargetDeviceName,exa_field_name=src_host""",
    """exa_json_path=$.properties.AccountDomain,exa_field_name=domain,exa_match_expr=!Contains(tolower($.properties.AccountDomain), "null")"""
    """exa_json_path=$.properties.AccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)),exa_match_expr=!Contains(tolower($.properties.AccountUpn), "null")""",
    """exa_json_path=$.properties.Protocol,exa_field_name=protocol,exa_match_expr=!Contains(tolower($.properties.Protocol), "")""",
    """exa_json_path=$.properties.DestinationIPAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.properties.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.properties.DestinationPort,exa_field_name=dest_port""",
    """exa_json_path=$.properties.Application,exa_field_name=app""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_regex=({event_name}Account Password changed)"""
  ]
  ParserVersion = "v1.0.0"


}
```