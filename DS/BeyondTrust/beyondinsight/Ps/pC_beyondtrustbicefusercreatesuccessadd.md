#### Parser Content
```Java
{
Name = beyondtrust-bi-cef-user-create-success-add
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|PBPS|RequestorApprover|""", """|BeyondTrust|BeyondInsight|""", """BeyondTrustBeyondInsightOperation=Add""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})""" """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """suser=({user}[^\s]+)"""
  """BeyondTrustBeyondInsightOperation=({operation}[^\s]+)"""
  """dst=({dest_ip}[A-fa-f\d:.]+)"""
  """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  """({app}BeyondInsight)"""
  """dhost=({account_domain}[^\/,]+?)[\/]+({account_name}[^,\s]+)"""
  ]


}
```