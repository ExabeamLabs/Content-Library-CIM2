#### Parser Content
```Java
{
Name = microsoft-defenderep-json-user-password-modify-success-passwordchanged
  Vendor = Microsoft
  Product = Microsoft Defender
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"category":""", """"AdvancedHunting-IdentityDirectoryEvents"""", """"ActionType":""",""""Account Password changed"""" ]
  Fields = [
    """exa_json_path=$..Timestamp,exa_field_name=time""",
    """exa_json_path=$..TargetDeviceName,exa_regex=({src_host}[\w\-\.]+)""",
    """exa_json_path=$..AccountDomain,exa_regex=(null|({domain}[^"]+))""",
    """exa_json_path=$..AccountUpn,exa_regex=(null|(({email_address}([A-Za-z0-9]+[!#$%&'+\/.=?^_`~-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}({first_name}[^.\s",]+)[.\s]+({last_name}[^",]+))|({user}[\w\.\-]{1,40}\$?)))""",
    """exa_json_path=$..AccountName,exa_regex=(null|(({email_address}([A-Za-z0-9]+[!#$%&'+\/.=?^_`~-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}({first_name}[^.\s",]+)[.\s]+({last_name}[^",]+))|({user}[\w\.\-]{1,40}\$?)))""",
    """exa_json_path=$..Protocol,exa_field_name=protocol,exa_match_expr=!Contains(tolower($..Protocol), "")""",
    """exa_json_path=$..DestinationIPAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$..IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..DestinationPort,exa_regex=({dest_port}\d+)""",
    """exa_json_path=$..Application,exa_field_name=app""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_regex=({event_name}Account Password changed)""",
    """exa_json_path=$.tenantId,exa_field_name=tenant_id""",
    """exa_json_path=$..AccountSid,exa_field_name=user_sid""",
    """exa_json_path=$..TargetAccountSid,exa_field_name=dest_user_sid""",
    """exa_json_path=$..DestinationDeviceName,exa_regex=({dest_host}[\w\-\.]+)"""

  ]
  ParserVersion = "v1.0.0"


}
```