#### Parser Content
```Java
{
Name = citrix-cgateway-str-user-read-receive-ldap-user-search-event
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """In receive_ldap_user_search_event""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^"]+)"*""",
    """({event_code}default AAA Message)"""
  ]


}
```