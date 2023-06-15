#### Parser Content
```Java
{
Name = citrix-cgateway-str-process-create-success-command
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """default """, """ CMD_EXECUTED""", """ Command """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)(\s*GMT)?\s+(|({host}[^\s]+))\s+\S+\s*:\s*default\s+\w+\s+CMD_EXECUTED""",
    """\sUser\s+(?:<unknown>|({user}\S+))(\s+\S+){2}\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sCommand\s+"({process_command_line}[^\n]+?)\s*-\s*Status""",
    """\sStatus\s+"({result}[^":]+)""",
    """\sCommand\s+"({process_path}({process_dir}[^\s"]*?[\\\/]+)?({process_name}[^\s\\\/"]+))(\s|")""",
  ]


}
```