#### Parser Content
```Java
{
Name = delinea-centrifyis-kv-process-create-success-suite
  ParserVersion = v1.0.0
  Vendor = Delinea
  Product = Centrify Infrastructure Services
  TimeFormat = "epoch"
  Conditions = [ 
"""AUDIT_TRAIL|Centrify Suite"""
"""dzdo command execution ends"""
]
  Fields = [
    """utc=({time}\d{13})""",
    """\d+\|\d+\|({event_name}.+?)\|\d""",
    """pid=({process_id}\d+)""",
    """command=({process_path}({process_dir}.*?)(\/+({process_name}[^\/]+?))?)\s*(\w+=|$)"""
    """user=({user}[^\(\)\s\$]+)"""
    """status=({result}.+?)\s\w+=""",
    """parameters=({process_command_line}.+?)$"""
  ]


}
```