#### Parser Content
```Java
{
Name = beyondtrust-sra-cef-app-activity-success-pbwevent28693
  Vendor = BeyondTrust
  Product = BeyondTrust Secure Remote Access
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """PBW-EVENT-28693""", """|BeyondTrust|BeyondInsight|""", """cat=pbw""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """suser=(AD\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  """({app}BeyondInsight)"""
  """BeyondTrustBeyondInsightRuleName =({additional_info}[^=]+?)\s\w+="""
  ]


}
```