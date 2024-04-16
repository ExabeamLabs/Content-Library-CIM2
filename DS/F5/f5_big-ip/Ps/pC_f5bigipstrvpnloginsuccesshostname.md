#### Parser Content
```Java
{
Name = f5-bigip-str-vpn-login-success-hostname
    Vendor = F5
    Product = F5 BIG-IP
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """01490007:6:""", """: Session variable 'session.client.hostname' set to '""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[^\s]+)""",
      """:Common:({session_id}[^:]+)""",
      """hostname' set to '({src_host}[\w\-.]+)""",
    ]


}
```