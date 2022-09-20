#### Parser Content
```Java
{
Name = oam-am-kv-app-logout-success-logout
  Vendor = OAM
  Product = Access Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ IAU_RESOURCEHOST: """", """IAU_USERID: """", """ IAU_EVENTTYPE: "Logout""""  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-]\d\d:\d\d) ({host}[\w\-.]+)""",
    """IAU_USERID: "(null|Anonymous|GET_HIDE_COLUMN_LIST|({user}[^\s"@]+))"""",
    """IAU_USERID: "(null|Anonymous|({email_address}[^\s"@]+@[^\s"@]+))"""",
    """IAU_IDENTITYDOMAIN: "(null|({domain}[^\s"]+))"""",
    """IAU_INSTANCENAME: "(null|({target}[^"]+))"""",
    """IAU_REMOTEIP: "({src_ip}[A-Fa-f:\d.]+)"""",
    """IAU_CLIENTIPADDRESS: "({src_ip}[A-Fa-f:\d.]+)"""",
    """IAU_RESOURCEHOST: "(null|login|({app}[^"]+))"""",
    """IAU_EVENTTYPE: "(null|({operation}[^"]+))"""",
    """IAU_RESOURCEURI: "(null|({additional_info}[^"]+))"""",
    """IAU_AUTHENTICATIONPOLICYID: "(null|({object}[^"]+))"""",
    """IAU_AUTHORIZATIONPOLICYID: "(null|({object}[^"]+))"""",
    """IAU_RESOURCEID: "(null|({resource}[^"]+))"""",
    ]


}
```