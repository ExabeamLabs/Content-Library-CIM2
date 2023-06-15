#### Parser Content
```Java
{
Name = hp-arubacpm-cef-radius-traffic-success-authsource
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """"network/clearpass/""","""Error-Code""","""Auth-Source""", """Auth-Method""", """"message":""" ]
  Fields = [
    """Common\.Request-Timestamp\\=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[+-]\d+)""",
    """"host":"({host}[^"]+)"""",
    """Common\.Username\\=(({user_type}host)\/)?(({domain}[^\/]+)\/)?({email_address}[^@]+@[^,]+)?(backup|({user}[^,]+)?)(,\w+\.\w+\\=)""",
    """Common\.Service(\\)?=({network}[^=]+?),\w+\.\w+(\\)?=""",
    """Common\.Host-MAC-Address(\\)?=({src_mac}[^,]+)""",
    """Common\.NAS-IP-Address(\\)?=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """RADIUS\.Auth-Method(\\)?=({auth_method}[^,]+)""",
    """Error-Code\\=({result}\d+)""",
    """({event_name}(?i)auth)""",
  ]
  DupFields = [ "host->auth_server" ]


}
```