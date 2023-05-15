#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-app-activity-success-change
Vendor = BeyondTrust
Product = BeyondInsight
ParserVersion = "v1.0.0"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [ """cat=Change""", """LEEF:""", """|BeyondTrust|BeyondInsight|""", """EventDesc=Cancelled""" ]
Fields = [
  """devTime=({time}\w{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})\s*"""
  """dst=({dest_ip}[a-fA-F:\d.]+)\s*"""
  """({app}BeyondInsight)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\sAccountName =(-|({email_user}[^@"\s]+@([^@"\s]+)))"""
  """\sAccountName =(-|([^@"\s]+@[^@"\s]+)|(({domain}[^\s]+?)[\\]+)?({user}[\w.-]+))"""
  """EventName =({operation}[^\s]+?)\s"""
]


}
```