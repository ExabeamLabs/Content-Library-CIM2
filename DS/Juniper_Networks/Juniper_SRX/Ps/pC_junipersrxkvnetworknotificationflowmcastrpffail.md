#### Parser Content
```Java
{
Name = juniper-srx-kv-network-notification-flowmcastrpffail
    Vendor = Juniper Networks
    Product = Juniper SRX
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """FLOW_MCAST_RPF_FAIL""", """Juniper""" ]
    Fields = [
        """destination-address="({dest_ip}[^"]*)""",
        """\s({host}[^\s]*)\sRT_FLOW""",
        """source-address="({src_ip}[^"]*)""",
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
        """\sprotocol-name="({protocol}.*?)"""",
        """\sinterface-name="({src_interface}.*?)"\s"""
        """({event_name}FLOW_MCAST_RPF_FAIL)"""
    ]
    ParserVersion = "v1.0.0"


}
```