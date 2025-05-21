#### Parser Content
```Java
{
Name = "unix-unix-cef-endpoint-login-success-sessionopened"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch"
Conditions = [
"""|Unix|Unix|"""
"""|session opened|"""
"""cs1=su """
""" by (uid"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
""" dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""" dhost=({dest_host}[^\s]+)"""
]
DupFields = [
"dest_host->host"
]
ParserVersion = "v1.0.0"


}
```