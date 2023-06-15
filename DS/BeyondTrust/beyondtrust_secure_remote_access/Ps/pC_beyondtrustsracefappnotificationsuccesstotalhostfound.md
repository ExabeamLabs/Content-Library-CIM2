#### Parser Content
```Java
{
Name = beyondtrust-sra-cef-app-notification-success-totalhostfound
  Vendor = BeyondTrust
  Product = BeyondTrust Secure Remote Access
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """BeyondTrustBeyondInsightEventName =Total hosts found""", """BeyondTrust|BeyondInsight""" ]
  Fields = [
  """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})""" """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """BeyondTrustBeyondInsightClientHost=({src_host}[\w\-\.]+)"""
  """BeyondTrustBeyondInsightEventName =({event_name}[^\s]+)"""
  """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)"""
  """({app}BeyondInsight)"""
  """BeyondTrustBeyondInsightSubjectDescription=({additional_info}[^=]+?)\s\w+="""
  ]


}
```