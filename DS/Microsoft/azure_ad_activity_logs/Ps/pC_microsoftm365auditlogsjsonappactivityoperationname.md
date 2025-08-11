#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-app-activity-operationname
  Vendor = Microsoft
  Product = Azure AD Activity Logs
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a"]
  Conditions = [ """Microsoft.aadiam""", """tenantId":"""", """operationName"""]
  Fields = [
    """tenantId":"({host}[^",]+)""",
    """"?time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)""",
    """"time":"({time}\d{1,2}\/\d{1,2}\/\d{4} \d{2}:\d{2}:\d{2} (?:AM|PM))""",
    """"userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """initiatedBy":.+?id":"({user_uid}[^",]+)""",
    """callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """operationName":"({operation}[^",]+)""",
    """"result":"({result}[^",]+)""",
    """"app":\{[^\}]+?displayName":"({app}[^",]+)""",
    """"riskLevel":"(none|({alert_severity}[^"]+))""""
    """"?category":"({category}[^",]+)""",
    """"identity":"(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"]+))"[^=]+?"category":"(?:RiskyUsers|UserRiskEvents)"""",
    """"category":"(?:RiskyUsers|UserRiskEvents)"[^=]+?"identity":"(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"]+))"""",
    """"category":"(?!RiskyUsers|UserRiskEvents|ProvisioningLogs)[^"]+"[^=]+?"identity":"({app}[^"]+)"""",
    """"identity":"({app}[^"]+)"[^=]+?"category":"(?!RiskyUsers|UserRiskEvents|ProvisioningLogs)[^"]+"""",
    """"?loggedByService":\s*"(?:Account Provisioning|Core Directory|({app}[^",]+))"?""",
    """targetResources":.+?type":"({object}[^",]+)""",
    """"targetResources":.+?"displayName":"({dest_host}[\w\-.]+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\dZ)"""",
    """"resultReason":"({result_reason}[^"]+?)"""",
    """"description":"({additional_info}[^"]+?)"""",
    """"correlationId":"({correlation_id}[^"]+?)"""",
    """"tenantId":"({tenant_id}[^"]+?)"""",
    """"ErrorCode":"({error_code}[^"]+?)"""",
    """servicePrincipalName":"({attribute}[^",]+)"""",
    """"servicePrincipalId":\s*"(null|({principal_id}[^"]+))""""
  ]
  ParserVersion = "v1.0.0"


}
```