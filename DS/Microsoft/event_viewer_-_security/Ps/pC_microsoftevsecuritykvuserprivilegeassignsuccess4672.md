#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-assign-success-4672
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = ["""Se asignaron privilegios especiales a un nuevo inicio de sesión""", """Nombre de cuenta:""", """EventCode=4672"""]
  Fields = [
   """Message=({event_name}Se asignaron privilegios especiales a un nuevo inicio de sesión)""",
   """({event_code}4672)""",
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """Keywords=({action}[^=]+?)\s*TaskCategory=""",
   """Nombre de cuenta:\s*(-|SYSTEM|({user}[^\s]+))\s*Dominio de cuenta:\s*({domain}[^\s]+)\s*""",
   """Id. de inicio de sesión:\s*({login_id}[^\s]+)\s*Privilegios:\s*({privileges}[^\:]+?)?\s*$""",
  ]
  DupFields = ["host->dest_host"]


}
```