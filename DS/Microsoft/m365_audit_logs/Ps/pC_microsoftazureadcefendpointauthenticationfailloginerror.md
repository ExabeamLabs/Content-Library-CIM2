#### Parser Content
```Java
{
Name = "microsoft-azuread-cef-endpoint-authentication-fail-loginerror"
Vendor = "Microsoft"
Product = "M365 Audit Logs"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Azure Active Directory|"""
"""|PasswordLogonInitialAuthUsingPassword|"""
"""LoginError"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wact=({event_code}.+?)\s*(\w+=|$)"""
"""\Woutcome=({result}.+?)\s*(\w+=|$)"""
"""\Wsuid=(?!\S+@\S+)({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)"""
"""\Wsuid=({email_address}({user}[\w\.\-]{1,40}\$?)@[^\s]+)\s*(\w+=|$)"""
"""\Wshost=({src_host}[\w\-.]+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```