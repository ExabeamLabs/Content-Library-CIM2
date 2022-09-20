#### Parser Content
```Java
{
Name = siteminder-s-kv-app-activity-azreject
  Product = SiteMinder
  Vendor = SiteMinder
  ParserVersion = "v1.0.0"
  Conditions = [ """AzReject """, """,o=""" ]

siteminder-web-activity = {
  Product = SiteMinder
  Vendor = SiteMinder
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Fields = [
    """({action}AzAccept|ValidateAccept|AzReject) ({host}[\w\-.]+) \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] "({src_ip}[A-Fa-f:\d.]+)""",
    """(uid=({user}[^\s,]+),o=({group_name}[^,]+),dc=({domain}[^,"]+)|cn=({=user}[^\s,]+),ou=({=domain}[^,]+),o=({=group}[^,"]+)).*?"\s+"({web_domain}\S+) ({method}\S+) ({uri_path}[^"\s\?]+)({uri_query}\?[^"]*)?""""
  
}
```