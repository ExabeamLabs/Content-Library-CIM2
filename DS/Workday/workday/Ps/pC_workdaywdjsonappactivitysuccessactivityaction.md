#### Parser Content
```Java
{
Name = "workday-wd-json-app-activity-success-activityaction"
Vendor = "Workday"
Product = "Workday"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""activityAction":"""
""""tenantHost":"""
"""workday"""
]
Fields = [
""""userAgent":\s*"({user_agent}[^"]+)"""
""""requestTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""deviceType":\s*"({device_type}[^"]+)"""
""""systemAccount":\s*";*({user}[^;"]+)"""
""""tenantHost":\s*"({host}[^"]+)"""
""""activityAction":\s*"({additional_info}[^"]+)"""
""""ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""target":\s*\{[^\}]*"descriptor":\s*"({object}[^"]+?)""""
""""taskDisplayName":\s*"({operation}[^"]+)"""
"""({app}(W|w)orkday)"""
]
ParserVersion = "v1.0.0"


}
```