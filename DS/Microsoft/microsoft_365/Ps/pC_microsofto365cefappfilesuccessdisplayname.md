#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-file-success-displayname
  ParserVersion = v1.0.0
  Product = Microsoft 365
  TimeFormat = ${MSParsersTemplates.cef-microsoft-app-activity.TimeFormat}["yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """destinationServiceName =Office 365""", """"activityDisplayName":"""" ]
  Fields = ${MSParsersTemplates.cef-microsoft-app-activity.Fields}[
    """"result"+:"+({result}[^"]+)""",
    """"resultReason":"(|({result_reason}.+?))",""""
    """"activityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
    """modifiedProperties"+:\[\{[^\}]+\},\{[^\}]+?"+newValue"+:"+\\"+({object}[^\\"]+?)\s*\\?"""",
    """"targetResources"+:\[[^\]]+?"+displayName"+:"+({target}[^"]+?)\s*"""",
    """"category"+:"+({additional_info}[^"]+)""",
    """"key":"MethodsUsedForValidation","value":"\[({additional_info}[^"]+)\]"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"initiatedBy"\s*:\s*\{[^\}]*?"user"\s*:\s*\{[^\}]*?"displayName"\s*:\s*"({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))"""
    """"initiatedBy"\s*:\s*\{[^\}]*?"user"\s*:\s*\{[^\}]*?"userPrincipalName"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """"app"+:\{[^\}]+?"displayName"+:"+({app}[^"]+)"""",
    """"DeviceOSType".*?newValue":"\[?\\?"({os}[^"\\]+)\\?"\]?"""
    """"Device OS.*?value":"({os}[^"]+)""""
    """\"key\":\"User-Agent\",\"value\":\"({user_agent}[^\"]+)\""""
    """"value":"({os}[^"]+)","key":"Device OS"""
  ]

cef-microsoft-app-activity = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"Host":"({host}[^"]+)"""",
    """"message":"({additional_info}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """category":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """resourceId":\s*"({object}[^"]+)""",
    """"Operation":\s*"({operation}[^"]+)""",
    """"operationName":"({operation}[^"]+)""",
    """"name":"({full_name}[^"]+)"""",
    """action":"({action}[^"]+)""",
    """"((?i)callerIpAddress|CIp)":"({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?"""",
    """claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"email":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """({app}Databricks)""",
    """"serviceName\\*":\\*"({app}[^"]+)""",
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
# port is removed
    """"(?i)userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({http_response_code}\d+)""",
    """"actionName":"({operation}[^"]+)""",
    """(?i)userId":"({user_upn}[^",]+)""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    """"UserType":"*({user_type}[^,}"]+)"*"""
    """"Platform":"({os}[^"]+)""""
    """"OriginatingServer":"({host}\w+)\s*(\([^\)]+?\))?(\\r\\n)?""""
    """"ClientInfoString":"({user_agent}[^"]+)","""
    """"BrowserName":"({browser}[^"]+)"""
    """"(Client|Source)IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?""""
    """"Workload":\s*"({app}[^"]+)""""
    #"""duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
  ]
  DupFields = [ "object->resource" 
}
```