#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-app-login-fail-loginfailure
Vendor = BeyondTrust
Product = BeyondInsight
ParserVersion = "v1.0.0"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [ """cat=Login Failure""", """LEEF:""", """|BeyondTrust|BeyondInsight|""" ]
Fields = [
"""devTime=({time}\w{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})\s*"""
"""IPAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sUserName =(-|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""\sUserName =(-|([^@"\s]+@[^@"\s]+)|(({domain}[^\s]+?)[\\]+)?({user}[\w.-]+))"""
"""({app}BeyondInsight)"""
"""Message=({failure_reason}[^=]+?)\s+(\w+=|")"""
"""ActionType=({operation}[^\s]+)\s*"""
]


}
```