#### Parser Content
```Java
{
Name = vmware-carbonblackedr-kv-alert-trigger-success-alerttriggerd
Vendor = VMware
Product = Carbon Black EDR
TimeFormat = "M/dd/yyyy H:mm:ss a"
Conditions = [
  """Bit9 event:"""
  """ file_name=""""
  """ subtype=""""
]
Fields = [
  """\sdate="({time}\d{1,2}\/\d{1,2}\/\d\d\d\d \d{1,2}:\d\d:\d\d (AM|PM|am|pm))""""
  """\sip_address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """\sip_address="({host}[^"\s]+?)""""
  """\shostname="([^"]+[\\\/]+)?({dest_host}[^"\s]+?)""""
  """\shostname="([^"]+[\\\/]+)?({host}[^"\s]+?)""""
  """\ssubtype="({alert_name}[^"]+?)""""
  """\ssubtype="({access}[^"]+?)(\s*\([^"]+)?""""
  """\stype="({alert_type}[^"]+?)""""
  """\susername="(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """\sfile_path="({file_path}(({file_dir}[^"]+)\\+)?({file_name}[^"\\]+))""""
  """\sfile_name="({file_name}[^"]+)""""
  """\sfile_hash="({new_hash}[^"]+)""""
  """\sprocess="({process_path}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```