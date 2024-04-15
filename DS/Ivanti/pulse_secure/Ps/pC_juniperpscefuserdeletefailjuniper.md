#### Parser Content
```Java
{
Name = "juniper-ps-cef-user-delete-fail-juniper"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|"""
"""|User deleted|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsuser=(System|({user}[^\s]+))"""
"""\Wduser=({dest_user}[^\s]+)"""
"""\Wshost=({src_host}[\w\-.]+)"""
"""\Wahost=({dest_host}.*?)\s\w+="""
]
DupFields = [
"dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```