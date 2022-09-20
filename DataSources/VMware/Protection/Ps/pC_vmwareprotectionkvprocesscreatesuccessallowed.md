#### Parser Content
```Java
{
Name = vmware-protection-kv-process-create-success-allowed
    ParserVersion = v1.0.0
    Vendor = VMware
    Product = Protection
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [ """Cb Protection event:""" , """subtype="Execution allowed""" , """ process=""" ]
    Fields = [
    """({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
    """\sdate="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
    """\stext="({additional_info}[^"]+)"""",
    """\ssubtype="({event_name}[^"]+)"""",
    """\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)"""",
    """\susername="(({domain}[^"\\]+)\\)?({user}[^"\\]+)"""",
    """\sip_address="({dest_ip}[a-fA-F\d.:]+)""",
    """\sprocess="({process_path}(({process_dir}[^"]+?)\\)?({process_name}[^"\\]+?))"""",
    """\sfile_path="({file_path}[^"]+)"""",
    """\sfile_name="({file_name}[^"]+)""""
   ]
   DupFields = [ "process_dir->process_path_directory" ]


}
```