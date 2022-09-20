#### Parser Content
```Java
{
Name = citrix-netscaler-str-process-create-success-command
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Netscaler VPN
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """default """, """ CMD_EXECUTED""", """ Command """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)(\s*GMT)?\s+({host}[^\s]+)\s+\S+\s*:\s*default\s+\w+\s+CMD_EXECUTED""",
    """\sUser\s+(?:<unknown>|({user}\S+))(\s+\S+){2}\s+({dest_ip}[a-fA-F\d.:]+)""",
    """\sCommand\s+"({process_command_line}[^"]+?)\s*"""",
    """\sStatus\s+"({result}[^":]+)""",
    """\sCommand\s+"({process_path}({process_dir}[^\s"]*?[\\\/]+)?({process_name}[^\s\\\/"]+))(\s|")""",
  ]


}
```