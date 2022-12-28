#### Parser Content
```Java
{
Name = siteminder-symantecsm-kv-http-request-success-validateaccept
  Product = Symantec SiteMinder
  Vendor = SiteMinder
  ParserVersion = "v1.0.0"
  Conditions = [ """ValidateAccept """, """,o=""" ]

siteminder-web-activity = {
  Product = Symantec Siteminder
  Vendor = SiteMinder
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Fields = [
    """({action}AzAccept|ValidateAccept|AzReject) ({host}[\w\-.]+) \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] "({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """(uid=({user}[^\s,]+),o=({group_name}[^,]+),dc=({domain}[^,"]+)|cn=({=user}[^\s,]+),ou=({=domain}[^,]+),o=({=group}[^,"]+)).*?"\s+"({web_domain}\S+) ({method}\S+) ({uri_path}[^"\s\?]+)({uri_query}\?[^"]*)?""""
  
}
```