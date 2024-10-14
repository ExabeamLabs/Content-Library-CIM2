#### Parser Content
```Java
{
Name = "siteminder-symantecsm-kv-endpoint-authentication-fail-authreject"
Vendor = "SiteMinder"
Product = "Symantec SiteMinder"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = [
"""AuthReject """
""" ["""
"""] """"
]
Fields = [
"""({action}\w+) ({host}[\w\-.]+) \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] "(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?""",
"""cn=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=({domain}[^,]+),o=({group_name}[^,"]+)"\s+"({app}\S+)\s"""
""""({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? uid=({user}[\w\.\-\!\#\^\~]{1,40}\$?),o=({group_name}[^,]+),dc=({domain}[^,]+),.*?" "({app}.+?) \S+ ({resource}[^"\s]+)" \[.+?error:\s*({failure_reason}[^\(]+?)\s*\(({failure_code}[^\)]+)\)"""
"""\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=({top_domain}[^,]+),DC=({process_name}[^"]+)["\s]+({user_agent}[^"]+)\s+({method}(GET|POST))\s+({uri_path}[^"\s\?]+)({uri_query}\?[^"]*)?""""
"""comment:\s*({failure_reason}[^,\[\]]+)"""
]
ParserVersion = "v1.0.0"


}
```