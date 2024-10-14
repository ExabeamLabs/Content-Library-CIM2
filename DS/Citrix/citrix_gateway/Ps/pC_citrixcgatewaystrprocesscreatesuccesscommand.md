#### Parser Content
```Java
{
Name = citrix-cgateway-str-process-create-success-command
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = ["MM/dd/yyyy:HH:mm:ss Z","yyyy/MM/dd:HH:mm:ss z"]
  Conditions = [ """default """, """ CMD_EXECUTED""", """ Command """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+(\s*GMT)?)\s+(|({host}[^\s]+))\s+\S+\s*:\s*default\s+\w+\s+CMD_EXECUTED""",
    """\sUser\s+(?:<unknown>|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\S+){2}\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sCommand\s+"({process_command_line}[^\n]+?)"*\s*-\s*Status""",
    """\sStatus\s+"({result}[^":]+)""",
    """\sCommand\s+"({process_path}({process_dir}[^\s"]*?[\\\/]+)?({process_name}[^\s\\\/"]+))(\s|")""",
  ]


}
```