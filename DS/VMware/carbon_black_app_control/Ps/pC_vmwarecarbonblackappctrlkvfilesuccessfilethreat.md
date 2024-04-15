#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-kv-file-success-filethreat"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """Cb Protection event:"""
  """subtype=""""
  """file_threat="""
]
Fields = [
  """({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
  """\sdate="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))"""
  """\stext="({additional_info}[^"]+)""""
  """\stype="({file_type}[^"]+)""""
  """\ssubtype="({access}[^"]+)""""
  """\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)""""
  """\susername="(({domain}[^"\\]+)\\)?({user}[^"\\]+)""""
  """\sip_address="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sfile_path="({file_path}({file_dir}[^"]+?)(\\({file_name}[^"\\]+?))?)""""
  """\sfile_name="({file_name}[^"]+?(\.({file_ext}[^".]+?))?)""""
  """\sprocess="({process_path}(({process_dir}[^"]+?)\\)?({process_name}[^"\\]+?))""""
  """\sfile_hash="({file_hash}\w+)"""
]
DupFields = [
  "access->event_code"
]
ParserVersion = "v1.0.0"


}
```