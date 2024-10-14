#### Parser Content
```Java
{
Name = "ibm-st-csv-app-login-fail-sametimeauth"
Vendor = "IBM"
Product = "Sametime"
TimeFormat = ["MMM/dd/yyyy HH:mm:ss a","MM/dd/yyyy hh:mm:ss a"]
Conditions = [
""" sametime-auth """
""","FAILURE","""
]
Fields = [
"""({host}[\w\-.]+)\s+sametime-auth\s+[^"]*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(am|AM|pm|PM))","({result}[^"]+)","({app}[^"]+)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({operation}sametime-auth)"""
]
ParserVersion = "v1.0.0"


}
```