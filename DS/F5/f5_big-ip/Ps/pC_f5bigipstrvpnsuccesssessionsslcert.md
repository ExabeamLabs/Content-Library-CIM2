#### Parser Content
```Java
{
Name = f5-bigip-str-vpn-success-sessionsslcert
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """session.ssl.cert.subject""", """01490113:5:""" ]
  Fields = [
    """(\s|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\s""",
    """:({session_id}[^:]+):\ssession.ssl.cert.subject""",
    """CN=({user}[\w\-.]+)"""
  ]


}
```