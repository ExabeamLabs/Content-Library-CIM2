#### Parser Content
```Java
{
Name = extremenetworks-exos-str-endpoint-notification-success-aaa
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """AAA: """, """Msg from Master :""", """password authentication""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """user\s+({user}\w+)"""
    """Msg from Master\s*:\s*({event_name}.+?)$"""
    """\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
 ]


}
```