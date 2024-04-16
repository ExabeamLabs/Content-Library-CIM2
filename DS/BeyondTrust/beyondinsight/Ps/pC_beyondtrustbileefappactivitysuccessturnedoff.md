#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-app-activity-success-turnedoff
Vendor = BeyondTrust
Product = BeyondInsight
ParserVersion = "v1.0.0"
TimeFormat = ["MMM dd yyyy HH:mm:ss","MMMM dd yyyy HH:mm:ss"]
Conditions = [ """cat=Change""", """LEEF:""", """|BeyondTrust|BeyondInsight|""", """EventDesc=Account's auto-management setting has been turned OFF""" ]
Fields = [
"""devTime=({time}\w{3,4}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})\s*"""
"""({event_name}Account's auto-management setting has been turned OFF)"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""({app}BeyondInsight)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sAccountName =(-|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""\sAccountName =(-|([^@"\s]+@[^@"\s]+)|(({domain}[^\s]+?)[\\]+)?({user}[\w\.\-]{1,40}\$?))"""
"""EventName =({operation}[^\s]+?)\s"""
]


}
```