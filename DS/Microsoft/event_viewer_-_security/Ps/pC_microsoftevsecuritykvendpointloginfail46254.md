#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-4625-4
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  ParserVersion = "v1.0.0"
  Conditions = ["""Error de una cuenta al iniciar sesión""", """Nombre de cuenta:""", """EventCode=4625"""]
  Fields = [
   """Message=({event_name}Error de una cuenta al iniciar sesión)""",
   """({event_code}4625)""",
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """Sujeto:[^=]+?\s*Nombre de cuenta:\s*(-|({src_user}[^\s@]+?))[\s;]*Dominio de cuenta""",
   """Sujeto:[^=]+?\s*Dominio de cuenta:\s*(-|({src_domain}[^:;]+?))[\s;]*Id. de inicio de sesión:""",
   """Tipo de inicio de sesión:\s*({login_type}\d+)""",
   """Cuenta con error de inicio de sesión:\s*[^=]+\s*Id. de seguridad:\s*(?:\/?NULL SID|({user_sid}[^\s]+))\s*Nombre de cuenta:""",
   """Nombre de cuenta:\s*({user}[^\s]+)\s*Dominio de cuenta:\s*({domain}[^\s]+)\s*Información de error:""",
   """Estado:\s*(?:[^\s]+)\s*Subestado:\s*({result_code}[^\s]+)\s*Información de proceso:""",
   """Nombre de estación de trabajo:\s*({src_host_windows}[^\s]+)\s*Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Puerto de orig""",
  ]
  DupFields = ["host->dest_host"]


}
```