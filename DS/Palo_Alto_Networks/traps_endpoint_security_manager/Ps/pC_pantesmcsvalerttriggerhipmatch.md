#### Parser Content
```Java
{
Name = pan-tesm-csv-alert-trigger-hipmatch
  Vendor = Palo Alto Networks
  Product = Traps Endpoint Security Manager
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,HIPMATCH,""" ]
  Fields = [
        """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d ({host}\S+)""",
        """\w+ \d+ \d\d:\d\d:\d\d ({host}\S+) \d+,\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d,""",
        """,(\d+),({event_name}HIPMATCH),\d+,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),(({domain}[^,\\]+)\\+)?({user}[^\\\s,]+),([^,]+),({src_host}[^,]+),({os}[^,]+),({src_ip}[A-Fa-f:\d.]+),([^,]+),([^,]+),([^,]+),([^,]*,){2}({seq_num}\d*),([^,]+),""",#dl fields are removed
  ]
  ParserVersion = v1.0.0


}
```