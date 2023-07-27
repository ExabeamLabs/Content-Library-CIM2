#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-kv-process-create-success-execution
    ParserVersion = v1.0.0
    Vendor = VMware
    Product = Carbon Black App Control
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [ """Carbon Black App Control event:""" , """subtype="Execution allowed""" , """ip_address=""" ]
    Fields = [
      """\sdate="({time}\d{1,2}\/\d{1,2}\/\d{1,4}\s\d{1,2}:\d{1,2}:\d{1,2}\s(am|AM|PM|pm))"""",
    """\shostname="(({domain}[^\\]+)\\({host}[^"]+))""",
    """\susername="(({domain}[^\\]+)\\({user}[\w\.\-]{1,40}\$?))"""",
    """\ssubtype="({event_name}[^"]+)"""",
    """\sprocess="+({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+)))""",
    """\sfile_hash="({file_hash}[^"]+)"""",
    """\stext="({additional_info}[^"]+?)\s*"""",
    """\sip_address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sfile_path="({file_path}[^"]+)"""",
    """\sfile_name="({file_name}[^"]+)"""",
    """\spolicy="({policy_name}[^"]+)""""
   ]
DupFields = [
"process_dir->process_path_directory", "process_path_name->parent_process_path" , "process_path->path"
]


}
```