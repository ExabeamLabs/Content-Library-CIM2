#### Parser Content
```Java
{
Name = huawei-usg-kv-process-create-success-shell
  Vendor = Huawei
  Product = Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """SHELL/""", """ command=""", """ result=""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """\sip=({src_ip}[a-fA-F\d.:]+)""",
     """\suser=(({email_address}[^@,]+@[^@,]+)|({user}[^,]+))""",
     """\scommand=({process_command_line}({process_path}({process_dir}[^,]*?[\\\/]+)?({process_name}[^\\\/\s]+))[^,]*?),""",
     """\sresult=({result}\w+)""",
  ]
  ParserVersion = "v1.0.0"


}
```