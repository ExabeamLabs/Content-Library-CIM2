#### Parser Content
```Java
{
Name = "fsecure-policymanager-cef-alert-trigger-success-fsecure"
Vendor = "F-Secure"
Product = "F-Secure Client Security"
TimeFormat = "MM dd yyyy HH:mm:ss"
Conditions = [
  """|F-Secure|F-Secure Client Security Premium|"""
  """domainTreePath="""
  """msg="""
]
Fields = [
  """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+"""
  """0\|F-Secure\|([^\|]+\|){4}({alert_severity}\d+)\|"""
  """(\s|\|)cs1=({malware_url}[^\s].+?)\s+(\w+=|$)"""
  """(\s|\|)act=({threat_category}[^\s].+?)\s+(\w+=|$)"""
  """(\s|\|)shost=({src_host}[^\s]+)"""
  """0\|F-Secure\|([^\|]+\|){2}({alert_name}[^\|]+)\|"""
  """\WRiskware:({alert_name}[^\s]+)"""
  """Family:\s+Name:\s*({alert_name}[^\s]+)"""
  """(\s|\|)cs2=({alert_name}[^\s].+?)\s+(\w+=|$)"""
  """0\|F-Secure\|([^\|]+\|){2}({alert_type}[^\|:]+):"""
  """\WType:\s*({alert_type}[^\s]+)"""
  """(\s|\|)suser=(({domain}[^\\=]+)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """(\s|\|)msg=({additional_info}[^\s].+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```