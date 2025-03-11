#### Parser Content
```Java
{
Name = extremenetworks-exos-str-endpoint-login-fail-aaa
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """AAA: """, """Login failed""", """for user""" ,"""through ssh""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """\d\d:\d\d:\d\d\s+({host}\w+)\s+AAA:"""
    """user\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """({event_name}Login ({result}failed))"""
    """({failure_reason}invalid username/password)"""
    """ssh\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
 ]


}
```