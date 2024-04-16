#### Parser Content
```Java
{
Name = "workday-wd-cef-app-login-success-authentication"
ParserVersion = "v1.0.0"
Vendor = "Workday"
Product = "Workday"
TimeFormat = "epoch"
Conditions = [
""""successful":true"""
""""signonDateTime":"""
"""workday"""
""""authenticationChannel":"""
]
Fields = [
"""destinationServiceName =({app}[^ ]+)"""
"""msg=({additional_info}[^=]+?)\s\w+=."""
"""\"signonIPAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"userName\":\"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
"""\"authenticationChannel\"+:\"+({auth_method}[^\"]+)"""
"""\"+authenticationType\"+:\"+({auth_method}[^\"]+)\"+"""
"""\"signonDateTime\"+:({time}\d{13})"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
"""\Wdproc=(|({dproc}[^=]+?))(\s+\w+=|\s*$)"""
]
DupFields = [ "auth_method->login_type_text" ]


}
```