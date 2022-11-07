#### Parser Content
```Java
{
Name = hp-arubaclearpass-cef-radius-traffic-success-authsource
  Vendor = HP
  Product = Aruba ClearPass Access Control and Policy Management
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """"ttam_category":"network/clearpass/""","""Error-Code""","""Auth-Source""" ]
  Fields = [
    """Common\.Request-Timestamp\\=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[+-]\d+)""",
    """"host":"({host}[^"]+)"""",
    """Common\.Username\\=(({user_type}host)\/)?(({domain}[^\/]+)\/)?({email_address}[^@]+@[^,]+)?(backup|({user}[^,]+)?)(,\w+\.\w+\\=)""",
    """Common\.Service(\\)?=({network}[^=]+?),\w+\.\w+(\\)?=""",
    """Common\.Host-MAC-Address(\\)?=({src_mac}[^,]+)""",
    """Common\.NAS-IP-Address(\\)?=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """RADIUS\.Auth-Method(\\)?=({auth_method}[^,]+)""",
    """Error-Code\\=({result}\d+)""",
    """({event_name}(?i)auth)""",
  ]
  DupFields = [ "host->auth_server" ]


}
```