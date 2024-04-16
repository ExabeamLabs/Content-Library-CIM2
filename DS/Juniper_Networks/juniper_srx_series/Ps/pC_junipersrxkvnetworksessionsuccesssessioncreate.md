#### Parser Content
```Java
{
Name = juniper-srx-kv-network-session-success-sessioncreate
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ 
"""RT_FLOW - RT_FLOW_SESSION_CREATE"""
"""encrypted="""
]
  Fields = [
    """encrypted=\"({additional_info}[^\"]*)""",
    """destination-address=\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """destination-port=\"({dest_port}\d*)""",
    """\s({event_name}RT_FLOW - [^\s]*)\s\[""",
    """\s({host}[^\s]*)\sRT_FLOW""",
    """packet-incoming-interface=\"({src_interface}[^\"]*)""",
    """source-address=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """source-port=\"({src_port}\d*)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?""",
    """username=\"(?!N\/A)({user}[\w\.\-]{1,40}\$?)\"""",
    """protocol-id=\"({protocol}[^\"]*)""",
    """destination-zone-name=\"({dest_network_zone}[^\"]*)""",
    """reason=\"({miscellaneous}[^\"]*)""",
    """\sapplication=\"({network_app}[^\"]*)""",
    """policy-name=\"({policy_name}[^\"]*)""",
    """source-zone-name=\"({src_network_zone}[^\"]*)""",
    """nested-application=\"({subtype}[^\"]*)""",
    """service-name=\"({service_name}[^\"]*)"""
  ]


}
```