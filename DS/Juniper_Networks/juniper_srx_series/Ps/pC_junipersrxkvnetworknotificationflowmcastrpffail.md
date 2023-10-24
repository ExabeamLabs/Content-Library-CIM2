#### Parser Content
```Java
{
Name = juniper-srx-kv-network-notification-flowmcastrpffail
    Vendor = Juniper Networks
    Product = Juniper SRX Series
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """FLOW_MCAST_RPF_FAIL""", """Juniper""" ]
    Fields = [
        """destination-address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """\s({host}[^\s]*)\sRT_FLOW""",
        """source-address="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
        """\sprotocol-name="({protocol}.*?)"""",
        """\sinterface-name="({src_interface}.*?)"\s"""
        """({event_name}FLOW_MCAST_RPF_FAIL)"""
    ]
    ParserVersion = "v1.0.0"


}
```