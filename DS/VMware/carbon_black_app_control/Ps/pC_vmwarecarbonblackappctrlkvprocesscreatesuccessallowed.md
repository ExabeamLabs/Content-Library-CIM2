#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-kv-process-create-success-allowed
    ParserVersion = v1.0.0
    Vendor = VMware
    Product = Carbon Black App Control
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [ """Cb Protection event:""" , """subtype="Execution allowed""" , """ process=""" ]
    Fields = [
    """({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
    """\sdate="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
    """\stext="({additional_info}[^"]+)"""",
    """\ssubtype="({event_name}[^"]+)"""",
    """\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)"""",
    """\susername="(({domain}[^"\\]+)\\)?({user}[\w\.\-]{1,40}\$?)"""",
    """\sip_address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sprocess="({process_path}(({process_dir}[^"]+?)\\)?({process_name}[^"\\]+?))"""",
    """\sfile_path="({file_path}[^"]+)"""",
    """\sfile_name="({file_name}[^"]+)""""
   ]
   DupFields = [ "process_dir->process_path_directory" ]


}
```