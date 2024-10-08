#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-logout-success-4634
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""Se cerró sesión en una cuenta""", """EventCode=4634"""]
  Fields = [
   """Message=({event_name}Se cerró sesión en una cuenta)""",
   """({event_code}4634)""",
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """Id. de seguridad:\s*(NT AUTHORITY\\SYSTEM|({user_sid}[^\s]+))\s*Nombre de cuenta:""",
   """Nombre de cuenta:\s*({user}[\w\.\-]{1,40}\$?)\s*Dominio de cuenta:\s*({domain}[^\s]+)\s*Id. de inicio de sesión:\s*({login_id}[^\s]+)\s*Tipo de inicio de sesión:\s*({login_type}\d+)\s*""",
   """Keywords=({action}[^\=]+?)\s*TaskCategory=""",
  ]


}
```