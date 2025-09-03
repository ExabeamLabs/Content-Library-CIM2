#### Parser Content
```Java
{
Name = extremenetworks-exos-str-http-traffic-fail-snmp
 Vendor = Extreme Networks
 Product = EXOS
 ParserVersion = v1.0.0
 TimeFormat = "MMM  dd HH:mm:ss"
 Conditions = [ """SNMP access from source""", """SNMP.Master""", """Dropping this Request.""" ,"""denied by rule""" ]
 Fields = [
    """({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d)"""
    """\d\d:\d\d:\d\d\s+({host}\w+)\s+SNMP\.Master:"""
    """<SNMP\.Master\.({event_name}[^>]+)>"""
    """source\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """({result}denied)"""
    """({protocol}SNMP)"""
    """rule\s+({rule}\S+)\."""
  ]


}
```