#### Parser Content
```Java
{
Name = "cisco-duo-cef-app-login-fail-twofactorfail"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Duo Security|Two-Factor|"""
"""|FAILURE|"""
]
Fields = [
"""\|Duo Security\|({login_type_text}[^\|]+)\|[^\|]*\|({result}[^\|]+)\|"""
"""\scat=({failure_reason}.+?)\s+(\w+=|$)"""
"""\srt=({time}\d{13})"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
"""\ssproc=({app}.+?)\s+(\w+=|$)"""
"""\sdvc=({host}.+?)\s+(\w+=|$)"""
"""\sdvchost=({host}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```