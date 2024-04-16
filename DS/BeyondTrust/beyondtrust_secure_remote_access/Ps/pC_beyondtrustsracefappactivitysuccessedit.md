#### Parser Content
```Java
{
Name = beyondtrust-sra-cef-app-activity-success-edit
  Vendor = BeyondTrust
  Product = BeyondTrust Secure Remote Access
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMMM dd yyyy HH:mm:ss"]
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """act=Edit""", """|BeyondTrust|BeyondInsight|""", """fileType=""", """|AppAudit|Edit|""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})""" 
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """suser=({user}[\w\.\-]{1,40}\$?)"""
  """act=({operation}[^\s]+)""" """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  """({app}BeyondInsight)"""
  """fileType=({additional_info}[^=]+?)\s\w+="""
  ]


}
```