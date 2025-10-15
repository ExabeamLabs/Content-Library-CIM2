#### Parser Content
```Java
{
Name = microsoft-azuremon-json-endpoint-activity-success-catchall
   TimeFormat = [ "M/d/yyyy H:mm:ss.SSS"]
   ParserVersion = v1.0.0
   Conditions = [ """destinationServiceName =Azure""" , """ResourceId":"""" , """"category":"""" ]
   Fields = ${MSParserTemplates.microsoft-azure-endpoint-json.Fields}[
    """exa_regex=eventTimestamp":"({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+.\d\d\d)""",
    """exa_json_path=$.properties.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.properties.RawEventData.operationName,exa_field_name=operation""",
    """exa_json_path=$.properties.RawEventData.authorization,exa_regex=[^\]]+action\\?"[^,]+?"({action}[^,]+?)\\?""""
    """exa_json_path=$.properties.RawEventData.authorization,exa_regex=[^\]]+role\\?"[^,]+?"({role}[^,]+?)\\?""""
  ]
 

}
```