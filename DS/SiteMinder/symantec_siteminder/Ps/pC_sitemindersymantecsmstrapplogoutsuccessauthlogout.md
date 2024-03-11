#### Parser Content
```Java
{
Name = siteminder-symantecsm-str-app-logout-success-authlogout
  Vendor = SiteMinder
  Product = Symantec SiteMinder
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """ AuthLogout """, """ [""", """] """" ]
  Fields = [
    """:\s({result}[^:]+?)\s+({host}\S+)\s+\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d (\+|\-)\d+)\] "\s*({user_ou}cn=({user}[^,"]+)[^"]*)"""",
  ]
  ParserVersion = "v1.0.0"


}
```