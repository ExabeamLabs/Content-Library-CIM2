#### Parser Content
```Java
{
Name = "workday-wd-cef-app-login-fail-expired"
ParserVersion = "v1.0.0"
Vendor = "Workday"
Product = "Workday"
TimeFormat = "epoch"
Conditions = [
""""successful":false"""
""""signonDateTime":"""
"""workday"""
""""authenticationChannel":"""
]
Fields = [
"""destinationServiceName =({app}[^ ]+)"""
"""msg=({additional_info}[^=]+?)\s\w+=."""
"""\"signonIPAddress\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"userName\":\"({user}[^\"]+)"""
"""\"+authenticationType\"+:\"+({auth_method}[^\"]+)\"+"""
"""\"authenticationChannel\"+:\"+({auth_method}[^\"]+)"""
"""\"signonDateTime\"+:({time}\d{13})"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
"""\Wdproc=(|({dproc}[^=]+?))(\s+\w+=|\s*$)"""
"""\"authenticationFailureMessage\":\"({failure_reason}[^\"]+)"""
]


}
```