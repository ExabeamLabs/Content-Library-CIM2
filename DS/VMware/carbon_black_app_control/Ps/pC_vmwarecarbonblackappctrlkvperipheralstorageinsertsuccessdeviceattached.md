#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-deviceattached"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""Carbon Black App Control event:"""
"""subtype="Device attached"""
""" ip_address="""
]
Fields = [
    """\sdate="({time}\d{1,2}\/\d{1,2}\/\d{1,4}\s\d{1,2}:\d{1,2}:\d{1,2}\s(am|AM|PM|pm))"""",
    """\shostname="(({domain}[^\\]+)\\({host}[^"]+))"""",
    """\ssubtype="({operation}[^"]+)"""",
    """\stext="({operation_details}[^"]+?)\s*"""",
    """\sip_address="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\spolicy="({event_name}[^"]+)"""",
    """\(S\/N:\s*({device_id}[^\)]+)\)"""
]
ParserVersion = "v1.0.0"


}
```