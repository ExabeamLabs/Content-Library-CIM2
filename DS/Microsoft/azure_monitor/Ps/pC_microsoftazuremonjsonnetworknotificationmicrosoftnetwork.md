#### Parser Content
```Java
{
Name = microsoft-azuremon-json-network-notification-microsoftnetwork
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ExtractionType = json
  Conditions = [ """"resourceId":""", """"category":""", """MICROSOFT.NETWORK""", """"properties":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$..category,exa_field_name=category""",
    """exa_json_path=$.resourceId,exa_field_name=resource""",
    """exa_json_path=$..Protocol,exa_field_name=protocol""",
    """exa_json_path=$..SourceIp,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$..DestinationIp,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$..SourcePort,exa_field_name=src_port""",
    """exa_json_path=$..DestinationPort,exa_field_name=dest_port""",
    """exa_json_path=$..Action,exa_field_name=action""",
    """exa_json_path=$..Rule,exa_field_name=rule""",
    """exa_json_path=$..RuleCollection,exa_field_name=rule_type""",
    """exa_json_path=$..RuleCollectionGroup,exa_field_name=rule_source""",
    """exa_json_path=$..Policy,exa_field_name=policy_name""",
    """exa_json_path=$..PolicyType,exa_field_name=policy_type"""
  ]
  ParserVersion = v1.0.0


}
```