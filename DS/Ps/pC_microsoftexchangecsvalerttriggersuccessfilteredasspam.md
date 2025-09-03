#### Parser Content
```Java
{
Name = "microsoft-exchange-csv-alert-trigger-success-filteredasspam"
Conditions = [
""","FilteredAsSpam",""" 
]
ParserVersion = "v1.0.0"

json-microsoft-security-events-1.Fields}[
  """exa_regex="privateIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_regex="publicIpAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.id,exa_field_name=alert_id"""
  """exa_regex="domainName":\s*"({domain}[^"]+)",\s*"userPrincipalName"""
  """exa_regex="fqdn":\s*"({src_host}[^"]+)"""

}
```