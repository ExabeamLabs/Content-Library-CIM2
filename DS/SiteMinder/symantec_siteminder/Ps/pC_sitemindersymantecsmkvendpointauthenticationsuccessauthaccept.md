#### Parser Content
```Java
{
Name = "siteminder-symantecsm-kv-endpoint-authentication-success-authaccept"
Vendor = "SiteMinder"
Product = "Symantec SiteMinder"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = [
"""AuthAccept """
""",o="""
""";authlevel="""
]
Fields = [
"""({action}AuthAccept) ({host}[\w\-.]+) \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""cn=({user}[\w\.\-]{1,40}\$?),ou=({domain}[^,]+),o=({group_name}[^,"]+).*?"\s+"({web_domain}\S+)\s+({method}\S+)\s+({uri_path}[^"\?]+)(\?({uri_query}[^"]+))?""""
"""uid=({user}[\w\.\-]{1,40}\$?),o=({group_name}[^,]+),dc=({domain}[^,]+),.*?" "({app}.+?) \S+ ({resource}[^"\s]+)" \[.+?"""
"""authlevel=({auth_level}[^;\]]+)"""
]
ParserVersion = "v1.0.0"


}
```