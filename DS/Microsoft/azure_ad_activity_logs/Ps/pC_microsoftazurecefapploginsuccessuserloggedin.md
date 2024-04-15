#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-success-userloggedin"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Azure"""
"""UserLoggedIn"""
""" suid="""
]
Fields = [
"""\sact=({operation}.+?)\s+(\w+=|$)"""
"""\srt=({time}\d{13})"""
"""\soutcome=({result}.+?)\s+(\w+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdvc=({host}\S+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wduser=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
"""\Wsuser=({email_address}[^@\s]+@({email_domain}[^\s@]+))"""
"""\ssuid=(Unknown|({email_address}[^@]+@({email_domain}.+?)))\s+(\w+=|$)"""
"""CEF:([^\|]*\|){2}({app}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```