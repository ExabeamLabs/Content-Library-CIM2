#### Parser Content
```Java
{
Name = "microsoft-ata-cef-alert-trigger-success-ldapbruteforcesuspiciousactivity"
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
  """|Microsoft|ATA|"""
  """|LdapBruteForceSuspiciousActivity|"""
  """CEF:"""
]
Fields = [
  """Auth\.[^\s]+\s*({host}[^\s]+)"""
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """start=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """msg=({additional_info}[^=]+?)\s+(\w+=|$)"""
  """msg=[^=]*? from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\.\s]+))"""
  """cs1=({additional_info}[^=]+?)\s*"*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```