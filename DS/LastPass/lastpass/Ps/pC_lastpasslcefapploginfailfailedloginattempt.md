#### Parser Content
```Java
{
Name = "lastpass-l-cef-app-login-fail-failedloginattempt"
Vendor = "LastPass"
Product = "LastPass"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""Data":"""
"""Action":"Failed Login Attempt"""
"""dproc=EventReporting"""
"""destinationServiceName =LastPass"""
]
Fields = [
""""Time":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""IP_Address":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""destinationServiceName =({app}[^=]+?)\s\w+="""
""""+Action"+:"+({event_name}[^"]+)"+"""
""""Username"+:"+({user}[^@"]+@[^\."]+(\.[^"]+)?)"""
""""+Data"+:"+({additional_info}[^"\}]+)"""
]
ParserVersion = "v1.0.0"


}
```