#### Parser Content
```Java
{
Name = beyondtrust-bi-cef-user-create-success-add
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMMM dd yyyy HH:mm:ss"]
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|PBPS|RequestorApprover|""", """|BeyondTrust|BeyondInsight|""", """BeyondTrustBeyondInsightOperation=Add""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})""" 
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """suser=(({domain}[\w\.\-]{1,40}?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """BeyondTrustBeyondInsightOperation=({operation}[^\s]+)"""
  """dst=({dest_ip}[A-fa-f\d:.]+)"""
  """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  """({app}BeyondInsight)"""
  """dhost=(({account_domain}[^\/,\s]+?)[\\\/]+)?({dest_user}({account_name}[^,\s]+))"""
  """dhost=(Asset:({src_host}[^\s]+)\sAccount:)(({account_domain}[\w\.\-]+?)[\\]+)?({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]


}
```