#### Parser Content
```Java
{
Name = beyondtrust-bi-json-app-activity-success-cancel
  ParserVersion = v1.0.0
  Conditions = [ """"operation":"Cancel"""", """"vendor":"BeyondTrust"""", """"product":"BeyondInsight"""", """"eventdesc":""" ]

json-beyondtrust-activity = {
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """"eventdate":"({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """"sourcehost":"({host}[\w\-\.]+)""",
    """"sourceip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"user":"(({domain}[^\\\/]+)\\+)?(Internal process|({user}[\w\.\-]{1,40}\$?))""",
    """"operation":"({operation}[^"]+)""",
    """"failed":"({result}\d)""",
    """"ipaddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"target":"Asset:({dest_host}[\w\-\.]+)\sMAccount:({account}[\w\-\.]+)""",
    """"target":"Domain:[^:]+?MAccount:({account}[\w\-\.]+)""",
    """"target":"[^"]+?ManagedAccount=({account}[\w\-\.]+)""",
    """"target":"[^\/,]+\/({dest_host}[\w\-\.]+),\sAccount\s""",
    """({app}BeyondInsight)"""
    ]
 }

json-beyondtrust-activity-1 = {
  Vendor = BeyondTrust
  Product = BeyondInsight
  ExtractionType = json
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Fields = [
  """exa_json_path=$.TimeCreated,exa_field_name=time"""
  """exa_json_path=$.EventName,exa_field_name=event_code"""
  """exa_json_path=$.AssetName,exa_field_name=dest_host"""
  """exa_json_path=$.UserName,exa_regex=({domain}[^\\\/]+?)[\\\/]+({user}[\w\.\-]{1,40}\$?)"""
  """exa_regex=Path\":\"({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?))\""""
  """exa_json_path=$.UserType,exa_field_name=privileges"""
  """exa_json_path=$.RuleName,exa_field_name=event_name,exa_match_expr=!inlist($.RuleName,"NONE")"""

}
```