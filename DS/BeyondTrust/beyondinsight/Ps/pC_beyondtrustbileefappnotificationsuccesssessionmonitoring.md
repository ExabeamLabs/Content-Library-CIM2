#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-app-notification-success-sessionmonitoring
Vendor = BeyondTrust
Product = BeyondInsight
ParserVersion = "v1.0.0"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [ """cat=Session Monitoring""", """LEEF:""", """|BeyondTrust|BeyondInsight|""" ]
Fields = [
  """devTime=({time}\w{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})\s*"""
  """({app}BeyondInsight)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\susrName =(-|({email_user}[^@"\s]+@([^@"\s]+)))"""
  """\susrName =(-|([^@"\s]+@[^@"\s]+)|(({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """EventName =({operation}[^\s]+?)\s"""
  """IPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """Message=({additional_info}[^=]+?)\s+(\w+=|")"""
]


}
```