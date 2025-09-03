#### Parser Content
```Java
{
Name = extremenetworks-exos-str-endpoint-authentication-fail-snmp
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """Login failed through""", """SNMP""", """AuthFail>""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """\d\d:\d\d:\d\d\s+({host}\S+)\s+SNMP\.Master:"""    
    """({event_name}Login failed)"""
    """\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
    """({result}failed)"""
    """({protocol}SNMP)"""   
 ]


}
```