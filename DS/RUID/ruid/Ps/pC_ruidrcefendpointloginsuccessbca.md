#### Parser Content
```Java
{
Name = "ruid-r-cef-endpoint-login-success-bca"
Vendor = "RUID"
Product = "RUID"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|BCA|RUID|"""
""" cn1="""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wcs3=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\Wcs4=({account}[^\s]+)"""
"""\Wcs5=({src_host}[\w\-.]+)"""
"""\Wcs5Label=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))(:\d+)?\s"""
"""\Wcn1=({admin_id}[^\s]+)"""
"""\WflexString2=({full_name}.+?)\s+(\w+=|$)"""
"""\Wdhost=({dest_host}[^\s]+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```