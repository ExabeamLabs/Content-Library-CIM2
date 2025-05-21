#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-app-activity-success-office365"
Conditions = 
[ """"src-application-name":"Office 365"""", """"event-name":"authz-group-deleted"""", """initiatedBy":""", """"src-endpoint":"Graph Directory Audit logs"""", """"category":"GroupManagement"""" ]

ParserVersion = "v1.0.0"

json-microsoft-security-events-1.Fields}[
  """exa_regex="privateIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_regex="publicIpAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.id,exa_field_name=alert_id"""
  """exa_regex="domainName":\s*"({domain}[^"]+)",\s*"userPrincipalName"""
  """exa_regex="fqdn":\s*"({src_host}[^"]+)"""

}
```