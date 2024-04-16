#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-4688-4
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""Se creó un nuevo proceso""", """Dominio de cuenta:""", """EventCode=4688"""]
  Fields = [
   """Message=({event_name}Se creó un nuevo proceso)""",
   """({event_code}4688)""",
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
   """Firmante creador:\s*Identificador de seguridad:\s*({user_sid}[^\s]+)\s*Nombre de cuenta:\s*({user}[\w\.\-]{1,40}\$?)\s*Dominio de cuenta:\s*({domain}[^\s]+)\s*Identificador de inicio de sesión:\s*({login_id}[^\s]+)""",
   """Nombre del nuevo proceso:\s*(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Tipo de elevación de token:""",
  ]
  ParserVersion = "v1.0.0"


}
```