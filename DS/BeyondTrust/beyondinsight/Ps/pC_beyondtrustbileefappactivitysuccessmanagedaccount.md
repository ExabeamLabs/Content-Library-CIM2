#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-app-activity-success-managedaccount
Vendor = BeyondTrust
Product = BeyondInsight
ParserVersion = "v1.0.0"
TimeFormat = ["MMM dd yyyy HH:mm:ss","MMMM dd yyyy HH:mm:ss"]
Conditions = [ """cat=PMM Managed Account""", """LEEF:""", """|BeyondTrust|BeyondInsight|""" ]
Fields = [
"""devTime=({time}\w{3,4}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})\s*"""
"""\sUserName =(-|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""\sUserName =(-|([^@"\s]+@[^@"\s]+)|(({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""({app}BeyondInsight)"""
"""IPAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""PasswordHistory=({additional_info}[^=]+?)\s+(\w+=|")"""
]


}
```