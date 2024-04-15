#### Parser Content
```Java
{
Name = "imperva-securesphere-cef-app-login-fail-loginfailed"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|Imperva Inc.|SecureSphere"""
"""cat=SystemEvent"""
"""|Login failed|"""
]
Fields = [
"""\srt=({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
"""\ssuser=({user}.+?)\s*(\w+=|$)"""
"""\|Login failed for user ({user}[^\s\(\)]+)"""
"""\|Login failed for user.*?\(IP: ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? Reason: ({failure_reason}[^\|]+)\|"""
]
ParserVersion = "v1.0.0"


}
```