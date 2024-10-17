#### Parser Content
```Java
{
Name = "unix-unix-cef-endpoint-login-fail-passwordcheckfailed"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""Unix|Unix"""
"""|password check failed|"""
"""categoryOutcome=/Failure"""
"""unix_chkpwd"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wahost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"""
"""\Wagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WcategoryOutcome=\/?({result}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```