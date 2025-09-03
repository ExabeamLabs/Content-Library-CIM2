#### Parser Content
```Java
{
Name = extremenetworks-exos-str-ssh-close-success-aaa
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """AAA: """, """logout from ssh (""", """Administrative account (""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """account\s+\(?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """({event_name}logout from ssh)"""
    """ssh\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
 ]


}
```