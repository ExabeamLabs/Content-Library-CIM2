#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-app-activity-operationname
  Vendor = Microsoft
  Product = M365auditlogs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """Microsoft.aadiam""", """tenantId":"""", """operationName"""]
  Fields = [
    """tenantId":"({host}[^",]+)""",
    """time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)""",
    """initiatedBy":.+?userPrincipalName":"({email_address}[^",]+)""",
    """initiatedBy":.+?id":"({user_uid}[^",]+)""",
    """callerIpAddress":"({src_ip}[^",]+)""",
    """operationName":"({operation}[^",]+)""",
    """result":"({result}[^",]+)""",
    """category":"({category}[^",]+)"*,correlationId"""",
    """"app":\{.*?displayName":"({app}[^",]+)""",
    """identity":"({app}[^",]+)""",
    """loggedByService":"({app}[^",]+)""",
    """targetResources":.+?type":"({object}[^",]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```