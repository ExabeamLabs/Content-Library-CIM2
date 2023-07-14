#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-success-groupadd
  Product = Microsoft 365
  ParserVersion = v1.0.0
  Conditions= [ """"activityType":"Group"""", """"activityOperationType":"Add"""", """"targetResourceType":"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.json-microsoft-app-activity.Fields} [
    """\sfname=\s*(N\/A|({object}[^=]+?))\s*(\w+=|$)""",
    """((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|([^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?))))\s+(\w+=|$)"""
  ]

json-microsoft-app-activity = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"activityDate":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"activity":"({operation}[^"]+)"""",
    """"(ipAddress|FromIP|ClientIP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"(UserId|userPrincipalName)":"({email_address}[^@]+@({email_domain}[^\.]+\.[^\]\s"\\,\|]+))",""",
    ""","value":"({email_address}[^@,]+@({email_domain}[^\.,]+\.[^\]\s",\|]+))"}]""",
    """"activityResultStatus":"({status}[^"]+)"""",
    """"category":"({category}[^"]+)"""",
    """"source":"({log_source}[^"]+)"""",
    """"activityType":"({object_type}[^"]+)"""",
    """"objectId":"({object_id}[^"]+)"""",
    """"correlationId":"({connection_id}[^"]+)"""",
    """\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)"""
    """\WdestinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)"""
    """\Wmsg=({additional_info}.*?)\s+(\w+=|$)""",
    """"name":"MethodsUsedForValidation","value":"\[({additional_info}[^"]+)\]"""",
    """"name":"DeviceOSType","value":"({os}[^"]+?)""""
  ]
  DupFields = [ "object->resource" 
}
```