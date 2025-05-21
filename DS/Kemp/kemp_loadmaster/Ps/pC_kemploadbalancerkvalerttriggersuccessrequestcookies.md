#### Parser Content
```Java
{
Name = "kemp-loadbalancer-kv-alert-trigger-success-requestcookies"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """ModSecurity:""",  """Warning""", """unique_id""", """severity""" ]
Fields = [
  """\[unique_id\s+"({alert_id}[^"]+)"""
  """\[hostname "({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """client:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\[severity\s+"({alert_severity}[^"]+)"""
  """({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d:\d\d)\s+({host}[\w\-\.]+) wafd"""
  """ModSecurity: Warning. Pattern match\s+"({additional_info}.+?)"\s+at REQUEST_COOKIES"""
  """\[file "(({file_path}({file_dir}[^\]]+)\/)?({file_name}[^"]+))"""
  """\[msg "({alert_name}[^"]+)"""
  """found within REQUEST_COOKIES:roHistory: \[({request_cookie}[^\]]+)"""
]


}
```