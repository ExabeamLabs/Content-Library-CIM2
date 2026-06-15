#### Parser Content
```Java
{
Name = microsoft-azuremon-json-endpoint-login-success-operationname
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","MM/dd/yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """microsoft.desktopvirtualization""", """"operationName":""", """"category":""" , """"ResourceType":"""" ]
  Fields = [
    """exa_json_path=$..time,exa_field_name=time""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$..resourceId,exa_field_name=resource_id""",
    """exa_json_path=$..resourceId,exa_regex=(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/)""",
    """exa_json_path=$..correlationId,exa_field_name=correlation_id""",
    """exa_json_path=$..callerIpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$..Level,exa_field_name=run_level""",
    """exa_json_path=$..user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_regex=(?i)IpAddress":\s*"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?""""
    """exa_json_path=$.identity.UserName,exa_regex=(({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$"""
    """exa_json_path=$..ActivityId,exa_field_name=activity_id""",
    """exa_regex=destinationServiceName =({app}[^\\s<]+)""",
    """exa_json_path=$.properties.State,exa_field_name=result""",
    """exa_json_path=$.properties.SessionHostName,exa_regex=({dest_host}[\w\-.]+)""",
    """exa_json_path=$.properties.SessionHostIPAddress,exa_regex=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.properties.ClientType,exa_field_name=client_type""",
    """exa_json_path=$.properties.ClientOS,exa_field_name=os""",
    """exa_json_path=$.properties.ClientVersion,exa_field_name=client_version""",
    """exa_json_path=$.properties.SessionHostOSVersion,exa_field_name=os_version""",
    """exa_json_path=$.properties.ClientLocationInfo,exa_field_name=location"""
    """exa_json_path=$.category,exa_field_name=event_category""",
    """exa_json_path=$..SessionHostPoolLocation,exa_regex=({host}[\w\-.]+)""",
    """exa_json_path=$.properties.GatewayRegion,exa_field_name=region"""
    """exa_json_path=$..ResourceType,exa_field_name=resource_type"""
  ]
  ParserVersion = v1.0.0


}
```