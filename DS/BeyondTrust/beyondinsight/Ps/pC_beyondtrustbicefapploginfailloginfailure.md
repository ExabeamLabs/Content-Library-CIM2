#### Parser Content
```Java
{
Name = beyondtrust-bi-cef-app-login-fail-loginfailure
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:0""", """|BeyondTrust|BeyondInsight|""", """|AppAudit|Login|""", """act=Login""", """fileType=""", """cat=Login Failure""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """suser=(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  """act=({operation}[^\s]+)"""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  """({app}BeyondInsight)"""
  """BeyondTrustBeyondInsightEventName =({event_name}[^\s]+?)\s*\w+="""
  """reason=({failure_reason}[^=]+?)\s*\w+="""
  ]


}
```