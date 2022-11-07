#### Parser Content
```Java
{
Name = juniper-srx-kv-app-notification-rtalgntcparseerr
    Vendor = Juniper Networks
    Product = Juniper SRX
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """RT_ALG_NTC_PARSE_ERR""", """Juniper""" ]
    Fields = [
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
        """\s({host}[^\s]*)\sjunos-alg""",
        """\sname="({protocol}.*?)"\s""",
        """\smessage="({additional_info}.*?)\s({src_ip}(\d{1,3}\.){3}\d{1,3})\/({src_port}\d+)->({dest_ip}(\d{1,3}\.){3}\d{1,3})\/({dest_port}\d+)"""",
        """({event_name}RT_ALG_NTC_PARSE_ERR)"""
    ]
    ParserVersion = "v1.0.0"


}
```