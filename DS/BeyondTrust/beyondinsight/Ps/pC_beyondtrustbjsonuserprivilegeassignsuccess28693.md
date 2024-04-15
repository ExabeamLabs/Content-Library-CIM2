#### Parser Content
```Java
{
Name = "beyondtrust-b-json-user-privilege-assign-success-28693"
Vendor = "BeyondTrust"
Product = "BeyondInsight"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """EventName":"28693"""
  """EventTypeID":"28693"""
  """Category":"pbw"""
  """UserType":""""
]
Fields = [
  """TimeCreated\":\"({time}\d+\/\d+\/\d\d\d\d\s\d+:\d+:\d+\s(am|AM|pm|PM))"""
  """EventName\":\"({event_code}\d+)\""""
  """AssetName\":\"({dest_host}[^\"]+?)\""""
  """UserName\":\"({domain}[^\\\/]+?)[\\\/]+({user}[^\"]+?)\""""
  """Path\":\"({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?))\""""
  """UserType\":\"({privileges}[^\"]+?)\""""
  """RuleName\":\"(NONE|({event_name}[^\"]+?))\""""
]
ParserVersion = "v1.0.0"


}
```