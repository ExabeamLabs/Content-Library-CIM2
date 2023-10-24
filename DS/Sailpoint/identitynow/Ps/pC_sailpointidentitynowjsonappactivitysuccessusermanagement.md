#### Parser Content
```Java
{
Name = "sailpoint-identitynow-json-app-activity-success-usermanagement"
Vendor = "Sailpoint"
Product = "IdentityNow"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""type": "USER_MANAGEMENT""""
""""stack": """"
""""attributes":"""
]
Fields = [
""""created":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""hostName":\s*"(\d+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^",]+))""""
""""ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""action":\s*"({operation}[^"]+)""""
""""type":\s*"({operation_type}[^",]+)""""
""""actor":[^\}]+?"name":\s*"(Not Available|unknown|({full_name}[^\s",]+(|,)\s[^\s",]+)|({user}[\w\.\-]{1,40}\$?))""""
""""technicalName":\s*"({event_name}[^",]+)""""
""""status":\s*"({result}[^",]+)""""
""""sourceName":\s*"({app}[^",]+)""""
""""info":\s*"(NONE|({additional_info}[^",]+))""""
]
ParserVersion = "v1.0.0"


}
```