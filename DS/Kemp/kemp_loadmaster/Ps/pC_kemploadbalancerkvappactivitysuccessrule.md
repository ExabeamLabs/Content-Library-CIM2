#### Parser Content
```Java
{
Name = "kemp-loadbalancer-kv-app-activity-success-rule"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ParserVersion = v1.0.0
Conditions = [ """ModSecurity:""",  """Rule""", """meta sequenceId""", """client""" ]
Fields = [
  """\[unique_id\s+"({alert_id}[^"]+)"""
  """\[hostname "({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """client:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d:\d\d)\s+({host}[\w\-\.]+) wafd"""
  """\[file "({file_path}(({file_dir}[^\]]+)\/)?({file_name}[^"\\\/]+))""""
  """\[uri\s*"({uri_path}[^"]+)"\]"""
]


}
```