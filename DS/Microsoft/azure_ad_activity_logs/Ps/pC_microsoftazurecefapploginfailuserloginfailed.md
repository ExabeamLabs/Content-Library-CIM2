#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-fail-userloginfailed"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Azure"""
"""UserLoginFailed"""
""" suid="""
]
Fields = [
"""\sact=({operation}.+?)\s+(\w+=|$)"""
"""\srt=({time}\d{13})"""
"""\soutcome=({result}.+?)\s+(\w+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdvc=({host}\S+)"""
"""\sdvchost=({host}[\w\-.]+)"""
"""\sduser=({email_address}[^@\s]+@[^\s@]+)"""
"""\ssuser=({email_address}[^@\s]+@[^\s@]+)"""
"""\ssuid=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)"""
"""CEF:([^\|]*\|){2}({app}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```