#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-app-activity-operationname
  Vendor = Microsoft
  Product = Azure AD Activity Logs
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """Microsoft.aadiam""", """tenantId":"""", """operationName"""]
  Fields = [
    """tenantId":"({host}[^",]+)""",
    """time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)""",
    """initiatedBy":.+?userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """initiatedBy":.+?id":"({user_uid}[^",]+)""",
    """callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """operationName":"({operation}[^",]+)""",
    """"result":"({result}[^",]+)""",
    """category":"({category}[^",]+)"*,correlationId"""",
    """"app":\{.*?displayName":"({app}[^",]+)""",
    """identity":"({app}[^",]+)""",
    """loggedByService":"({app}[^",]+)""",
    """targetResources":.+?type":"({object}[^",]+)"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\dZ)"""",
    """"resultReason":"({result_reason}[^"]+?)"""",
    """"description":"({additional_info}[^"]+?)"""",
    """"correlationId":"({correlation_id}[^"]+?)"""",
    """"tenantId":"({tenant_id}[^"]+?)"""",
    """"ErrorCode":"({error_code}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```