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
"""({action}AuthReject)\s+({host}[\w\-.]+)\s+\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\]\s+"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+.*?((CN|cn)|((({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({user}[\w\.\-\!\#\^\~\@\[\`]{1,40}\$?)|({full_name}[\w\s]+)|))\")\s+\"(({app}[^\s]+)\s+\S+\s+(({resource}({uri_path}[^"\s\?]+)({uri_query}\?[^"]*)*))))"""
"""\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}([^=]+))),OU=({group_name}[^,]+)(.+?DC=({domain}[^,]+),DC=([^,"]+))(.?DC=({process_name}[^"]+)|["\s])+({user_agent}[^"]+)\s+(({method}(GET|POST))|\S+)\s+({uri_path}[^"\s\?]+)({uri_query}\?[^"]*)?""""
"""cn=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=({domain}[^,]+),o=({group_name}[^,"]+)"\s+"({app}\S+)\s"""
""""({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? uid=({user}[\w\.\-\!\#\^\~]{1,40}\$?),o=({group_name}[^,]+),dc=({domain}[^,]+),.*?" "({app}.+?) \S+ ({resource}[^"\s]+)" \[.+?error:\s*({failure_reason}[^\(]+?)\s*\(({failure_code}[^\)]+)\)"""
"""comment:\s*({failure_reason}[^,\[\]]+)"""
]
ParserVersion = "v1.0.0"


}
```