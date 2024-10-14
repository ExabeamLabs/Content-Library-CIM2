#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-spanish-4624
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""Se inició sesión correctamente en una cuenta""", """Nombre de cuenta:""", """EventCode=4624"""]
  Fields = [
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """EventCode=({event_code}4624)""",
   """Message=({event_name}Se inició sesión correctamente en una cuenta)""",
   """Tipo de inicio de sesión:\s*({login_type}\d+)""",
   """Nuevo inicio de sesión:\s*[^=]*?Nombre de cuenta:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*Dominio de cuenta:\s*(-|({domain}[^\s]+))[\s;]*Id. de inicio de sesión:""",
   """Nombre de proceso:\s*(?:-|({process_path}[^\s]))\s*Información de red:""",
   """Nombre de estación de trabajo\s*(-|[A-Fa-f:\d.]+|({src_host}[^\s;]+))[\s;]*Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Puerto de origen:\s*({src_port}\d+)""",
   """Id. de inicio de sesión:\s*({login_id}[^\s;]+)[\s;]*(Inicio de sesión vinculado|GUID de inicio de sesión)""",
   """Nuevo inicio de sesión: [\s;]*Id. de seguridad:\s*(NT AUTHORITY\\SYSTEM|({user_sid}[^\s;]+))(\s|;)""",
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  ]


}
```