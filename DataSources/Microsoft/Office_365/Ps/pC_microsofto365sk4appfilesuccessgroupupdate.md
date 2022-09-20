#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-file-success-groupupdate
  Product = Office 365
  ParserVersion = v1.0.0
  Conditions= [ """"activityType":"Group"""", """"activityOperationType":"Update"""", """"targetResourceType":"""" ]

json-microsoft-app-activity = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"activityDate":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"activity":"({operation}[^"]+)"""",
    """"(ipAddress|FromIP|ClientIP)":"({src_ip}[^"]+)"""",
    """"(UserId|userPrincipalName)":"({email_address}[^@]+@({email_domain}[^"]+))"""",
    """"activityResultStatus":"({result}[^"]+)"""",
    """"category":"({category}[^"]+)"""",
    """"source":"({log_source}[^"]+)"""",
    """"activityType":"({object_type}[^"]+)"""",
    """"id":"({object_id}[^"]+)"""",
    """"correlationId":"({connection_id}[^"]+)"""",
    """\WdestinationServiceName\s*=({app}[^=]+?)\s+(\w+=|$)""",
    """\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)"""
  ]
  DupFields = [ "object->resource" 
}
```