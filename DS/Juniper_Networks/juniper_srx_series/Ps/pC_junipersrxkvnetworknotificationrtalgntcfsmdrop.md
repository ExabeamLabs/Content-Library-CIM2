#### Parser Content
```Java
{
Name = juniper-srx-kv-network-notification-rtalgntcfsmdrop
    Vendor = Juniper Networks
    Product = Juniper SRX Series
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """RT_ALG_NTC_FSM_DROP""", """Juniper""" ]
    Fields = [
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
        """\s({host}[^\s]*)\sjunos-alg""",
        """\smessage="({additional_info}[^"]+?)""""
        """\sname="({protocol}.*?)"\s"""
        """({event_name}RT_ALG_NTC_FSM_DROP)"""
    ]
    ParserVersion = "v1.0.0"


}
```