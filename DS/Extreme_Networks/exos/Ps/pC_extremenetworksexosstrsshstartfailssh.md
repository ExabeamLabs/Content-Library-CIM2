#### Parser Content
```Java
{
Name = extremenetworks-exos-str-ssh-start-fail-ssh
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """SSH connection from source""", """has been denied""", """Rejecting connection.""" ,"""exsshd:""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """\d\d:\d\d:\d\d\s+({host}\w+)\s+exsshd:"""    
    """<exsshd\.({event_name}[^>]+)>"""
    """source\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """({result}denied)"""
    """({protocol}SSH)"""
    """access-list\s+({access_list}[^\s]+)\."""   
 ]


}
```