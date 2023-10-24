#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-close-success-4689-3
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""Se salió de un proceso""", """EventCode=4689"""]
  Fields = [
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """Message=({event_name}Se salió de un proceso)""",
   """({event_code}4689)""",
   """ Id. de seguridad:\s*({user_sid}[^\s]+)\s*Nombre de cuenta:\s*({user}[\w\.\-]{1,40}\$?)\s*Dominio de cuenta:\s*({domain}[^\s]+)\s*""",
   """Id. de inicio de sesión:\s*({login_id}[^\s]+)\s*Información de proceso:""",
   """Id. de proceso:\s*({process_id}[^\s]+)\s*Nombre de proceso:\s*(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Estado de salida:""",
   """Keywords=({action}[^\=]+?)\s*TaskCategory=""",
  ]


}
```