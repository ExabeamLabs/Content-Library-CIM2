#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-login-fail-userloginfailed
  ParserVersion = v1.0.0
  Product = Microsoft 365
  Conditions = [ """"Workload":""", """"AzureActiveDirectoryEventType":""", """"Operation":""",  """"UserLoginFailed"""", """"ResultStatus":""", """"ClientIP":"""  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-o365-app-login-2.Fields} [
    """"ResultStatusDetail":\s*"((?i)Success|({failure_reason}[^"]+))"""",
    """"LogonError":\s*"({failure_reason}[^"]+)""",
    """"Operation":\s*"UserLogin({result}[^"]+)""",
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """"Operation":\s*"({operation}[^"]+)""",
    """"ErrorNumber":\s*"({error_code}\d+)"""",
    """"OS.*?Value":\s*"({os}[^"]+)|"Value":\s*"({=os}[^"]+)",\s*"Name":\s*"OS"""",
    """"BrowserType.*?Value":\s*"({browser}[^"]+)|"Value":\s*"({=browser}[^"]+)",\s*"Name":\s*"BrowserType""""
    """suser=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """"UserId":\s*"({user_upn}[^",]+)""""
    """"ObjectId":\s*"({object_id}[^"]+?)"""",
    """"ApplicationId":\s*"({app_id}[^"]+)""""
    """"UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
    """"Client\\*"+:[\s\\]*"+({user_agent}[^"]*)""",
    """Workload"*:\s*"*({resource}[^"]+)"""",
    """"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object}[^"\\]{0,249}?))\s*"""",
    """"Client\\*"+:[\s\\]*"+({user_agent}[^"]*)""",
    """"(U|u)serAgent\\*"+:[\s\\]*"(|({user_agent}[\s\S]*?))\\*",""",
    """\{"+Name"+:[\s\\]*"+UserAgent"+,"+Value"+:"+({user_agent}[^"]+)"+\}""",
    """"+Value"+:\s*"+({user_agent}[^"]+)"+,\s*"+Name"+:[\s\\]*"+UserAgent"+\},""",
    """"ExtendedProperties"[^]]*?UserAgent"+,\s*"+Value"+:\s*"+({user_agent}[^"]+)""",
    """"Name":"RequestType","Value":"({request_type}[^"]+?)\s*""""
    """"Value":"({request_type}[^"]+?)\s*","Name":"RequestType""""
    ]
  DupFields = [ "error_code->failure_code" ]

cef-o365-app-login-2 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"UserId":\s*"({user_upn}[^",]+)"""",
    """"ClientIP":\s*"\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(\]:({src_port}\d+))?"""",
    """"Operation":\s*"({event_name}[^"]+)""",
    """"ResultStatus":\s*"({result}[^"]+)"""",
    """destinationServiceName =({app}Office 365)""",
    """"Name":\s*"UserAgent","Value":\s*"({user_agent}[^"]+?)\s*"""",
    """"Workload":\s*"({app}[^"]+)"""
    
}
```