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
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"initiatedBy"\s*:\s*\{[^\}]*?"user"\s*:\s*\{[^\}]*?"displayName"\s*:\s*"({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))"""
    """"initiatedBy"\s*:\s*\{[^\}]*?"user"\s*:\s*\{[^\}]*?"userPrincipalName"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """"app"+:\{[^\}]+?"displayName"+:"+({app}[^"]+)"""",
    """"DeviceOSType"[^\}]+?"newValue":"[\[\\"]*({os}[\w\s]+?)[\\"\]]*\},"""
    """"Device OS.*?value":"({os}[^"]+)""""
    """\"key\":\"User-Agent\",\"value\":\"({user_agent}[^\"]+)\""""
    """"value":"({os}[^"]+)","key":"Device OS"""
    """appId":"({app_id}[^"]+)""""
  ]


}
```