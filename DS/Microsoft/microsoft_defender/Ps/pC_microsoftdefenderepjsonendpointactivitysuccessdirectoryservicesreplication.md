#### Parser Content
```Java
{
Name = microsoft-defenderep-json-endpoint-activity-success-directoryservicesreplication
  Vendor = Microsoft
  Product = Microsoft Defender
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ssZ" ]
  Conditions = [ """"category":""", """"AdvancedHunting-IdentityDirectoryEvents"""", """"ActionType":"""" ]
  Fields = [
    """exa_json_path=$..Timestamp,exa_field_name=time""",
    """exa_json_path=$..TargetDeviceName,exa_field_name=src_host""",
    """exa_json_path=$..AccountDomain,exa_regex=(?i)(((https|http):\/\/))?(null|-|NT AUTHORITY|({domain}[^\s\]"]+))""",
    """exa_json_path=$..AccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$..Protocol,exa_field_name=protocol""",
    """exa_json_path=$..DestinationIPAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$..IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..DestinationPort,exa_field_name=dest_port""",
    """exa_json_path=$..Application,exa_field_name=app""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$..ActionType,exa_field_name=event_name""",
    """exa_json_path=$..AdditionalFields.AttackTechniques,exa_field_name=additional_info""",
    """exa_json_path=$..AdditionalFields.IsSuccess,exa_field_name=result""",
    """exa_json_path=$..TargetAccountUpn,exa_field_name=user_upn"""
    """exa_json_path=$..AccountName,exa_field_name=account"""
    """exa_json_path=$..SourceAccountSid,exa_field_name=user_sid"""
    """exa_json_path=$..DestinationDeviceName,exa_field_name=dest_host"""
  ]
  ParserVersion = "v1.0.0"


}
```