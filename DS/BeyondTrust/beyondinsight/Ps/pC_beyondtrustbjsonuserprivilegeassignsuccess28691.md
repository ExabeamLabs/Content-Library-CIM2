#### Parser Content
```Java
{
Name = "beyondtrust-b-json-user-privilege-assign-success-28691"
Conditions = [
  """EventMessage":"Application Requested Elevation"""
  """EventName":"28691"""
  """Category":"pbw"""
  """UserType":"""
]
ParserVersion = "v1.0.0"

json-beyondtrust-activity-1 = {
  Vendor = BeyondTrust
  Product = BeyondInsight
  ExtractionType = json
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Fields = [
  """exa_json_path=$.TimeCreated,exa_field_name=time"""
  """exa_json_path=$.EventName,exa_field_name=event_code"""
  """exa_json_path=$.AssetName,exa_field_name=dest_host"""
  """exa_json_path=$.UserName,exa_regex=({domain}[^\\\/]+?)[\\\/]+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_regex=Path\":\"({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?))\""""
  """exa_json_path=$.UserType,exa_field_name=privileges"""
  """exa_json_path=$.RuleName,exa_field_name=event_name,exa_match_expr=!inlist($.RuleName,"NONE")"""

}
```