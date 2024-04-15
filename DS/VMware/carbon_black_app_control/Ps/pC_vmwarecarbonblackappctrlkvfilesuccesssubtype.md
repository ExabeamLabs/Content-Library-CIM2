#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-kv-file-success-subtype"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """Carbon Black App Control event:"""
  """subtype=""""
  """ ip_address="""
]
Fields = [
  """\sdate="({time}\d{1,2}\/\d{1,2}\/\d{1,4}\s\d{1,2}:\d{1,2}:\d{1,2}\s(am|AM|PM|pm))""""
  """\shostname="(({domain}[^\\]+)\\({host}[^"]+))"""
  """\susername="(({domain}[^\\]+)\\({user}[^"]+))""""
  """\ssubtype="({event_name}[^"]+)""""
  """\sprocess="+({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+)))"""
  """\sfile_hash="({file_hash}[^"]+)""""
  """\stext="({additional_info}[^"]+?)\s*""""
  """\sip_address="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\srule_name="({operation}[^"]+)""""
  """\sprocess_threat="({alert_severity}[^"]+)""""
  """\sfile_path="({file_path}[^"]+)""""
  """file_name="({file_name}[^"]+\.({file_ext}[^"]+))"""
  """\spolicy="({policy_name}[^"]+)""""
]
DupFields = [
  "event_name->access"
]
ParserVersion = "v1.0.0"


}
```