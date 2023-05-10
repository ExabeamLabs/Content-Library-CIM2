#### Parser Content
```Java
{
Name = juniper-srx-kv-app-notification-rtalgwrncfgneed
    Vendor = Juniper Networks
    Product = Juniper SRX Series
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """RT_ALG_WRN_CFG_NEED""", """Juniper""" ]
    Fields = [
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
        """\s({host}[^\s]*)\sjunos-alg""",
        """\sname="({protocol}.*?)"\s""",
        """message="detected packet from\s({src_ip}(\d{1,3}\.){3}\d{1,3})\/({src_port}\d+)\s"""
        """({event_name}RT_ALG_WRN_CFG_NEED)"""
    ]
    ParserVersion = "v1.0.0"


}
```