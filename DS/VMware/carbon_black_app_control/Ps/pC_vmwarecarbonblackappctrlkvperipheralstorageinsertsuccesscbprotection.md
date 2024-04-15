#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-kv-peripheral-storage-insert-success-cbprotection"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""Cb Protection event:"""
"""subtype="Device attached"""
]
Fields = [
"""({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
"""\sdate="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))"""
"""\stext="({operation_details}[^"]+)""""
"""\ssubtype="({event_code}[^"]+)""""
"""\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)""""
"""\susername="(({domain}[^"\\]+)\\)?({user}[^"\\]+)""""
"""\sip_address="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sprocess="({process_path}(({process_dir}[^"]+?)\\)?({process_name}[^"\\]+?))""""
"""Device '({device_type}[^'(]+?)\s*\("""
"""\(S\/N:\s*({device_id}[^)]+)\)"""
]
ParserVersion = "v1.0.0"


}
```