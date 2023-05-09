#### Parser Content
```Java
{
Name = beyondtrust-bi-cef-app-logout-success-logout
  Vendor = BeyondTrust
  Product = BeyondInsight
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """act=Logout""", """|BeyondTrust|BeyondInsight|""", """fileType=Logout""", """|AppAudit|Logout|""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """suser=({user}[^\s]+)"""
  """act=({event_name}[^\s]+)"""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """shost=({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  ]


}
```