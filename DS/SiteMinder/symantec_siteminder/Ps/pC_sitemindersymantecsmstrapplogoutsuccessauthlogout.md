#### Parser Content
```Java
{
Name = siteminder-symantecsm-str-app-logout-success-authlogout
  Vendor = SiteMinder
  Product = Symantec SiteMinder
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """AuthLogout """, """ [""", """] """" ]
  Fields = [
    """:\s({result}[^:]+?)\s+({host}\S+)\s+\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d (\+|\-)\d+)\] "\s*({user_ou}cn=({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^"]*)"""",
    """({action}AuthLogout)\s+({host}[\w\-.]+)\s+\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=({top_domain}[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\""""
  ]
  DupFields = [ "action->result" ]
  ParserVersion = "v1.0.0"


}
```