#### Parser Content
```Java
{
Name = extremenetworks-exos-str-endpoint-login-success-aaa
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """AAA: """, """Login passed for user""", """through ssh""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """user\s+({user}\w+)"""
    """({event_name}Login passed)"""
    """ssh\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
 ]


}
```