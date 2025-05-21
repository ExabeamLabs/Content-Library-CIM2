#### Parser Content
```Java
{
Name = huawei-usg-kv-process-create-success-shell
  Vendor = Huawei
  Product = Huawei Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """SHELL/""", """ command=""", """ result=""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """\sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """\suser=(({email_address}[^@,]+@[^@,]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
     """\scommand=({process_command_line}({process_path}({process_dir}[^,]*?[\\\/]+)?({process_name}[^\\\/\s]+))[^,]*?),""",
     """\sresult=({result}\w+)""",
  ]
  ParserVersion = "v1.0.0"


}
```