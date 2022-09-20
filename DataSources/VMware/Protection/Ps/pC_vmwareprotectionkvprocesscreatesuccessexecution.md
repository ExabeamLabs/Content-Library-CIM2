#### Parser Content
```Java
{
Name = vmware-protection-kv-process-create-success-execution
    ParserVersion = v1.0.0
    Vendor = VMware
    Product = Protection
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [ """Carbon Black App Control event:""" , """subtype="Execution allowed""" , """ip_address=""" ]
    Fields = [
      """\sdate="({time}\d{1,2}\/\d{1,2}\/\d{1,4}\s\d{1,2}:\d{1,2}:\d{1,2}\s(am|AM|PM|pm))"""",
    """\shostname="(({domain}[^\\]+)\\({host}[^"]+))""",
    """\susername="(({domain}[^\\]+)\\({user}[^"]+))"""",
    """\ssubtype="({event_name}[^"]+)"""",
    """\sprocess="+({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+)))""",
    """\sfile_hash="({file_hash}[^"]+)"""",
    """\stext="({additional_info}[^"]+?)\s*"""",
    """\sip_address="({dest_ip}[a-fA-F\d.:]+)""",
    """\sfile_path="({file_path}[^"]+)"""",
    """\sfile_name="({file_name}[^"]+)"""",
    """\spolicy="({policy_name}[^"]+)""""
   ]
DupFields = [
"process_dir->process_path_directory", "process_path_name->parent_process_path" , "process_path->path"
]


}
```