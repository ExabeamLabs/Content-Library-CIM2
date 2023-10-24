#### Parser Content
```Java
{
Name = juniper-srx-kv-app-notification-rtalgntcparseerr
    Vendor = Juniper Networks
    Product = Juniper SRX Series
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """RT_ALG_NTC_PARSE_ERR""", """Juniper""" ]
    Fields = [
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
        """\s({host}[^\s]*)\sjunos-alg""",
        """\sname="({protocol}.*?)"\s""",
        """\smessage="({additional_info}.*?)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)->({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)"""",
        """({event_name}RT_ALG_NTC_PARSE_ERR)"""
    ]
    ParserVersion = "v1.0.0"


}
```