#### Parser Content
```Java
{
Name = unix-unix-json-endpoint-activity-success-command
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"STAT":""", """"UID":""", """"PID":""", """"COMMAND":""" ]
  Fields = [
    """<\d+>\s+({host}\S+)?\s""",
    """"+UID"+:\s"+({user_uid}[^"]*)""",
    """"+PID"+:\s"+({process_id}[^"]*)""",
    """"+COMMAND"+:\s"+({process_command_line}[^"]*)""",
  ]


}
```