#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-assign-success-4673-1"
ParserVersion = "v1.0.0"
Conditions = [ 
  """EventCode=4673"""
  """Microsoft Windows security auditing"""
  """Message=Se llamó a un servicio con privilegios"""
]
Fields = ${WindowsParsersTemplates.spanish-windows-events.Fields}[
  """\s*Dominio de cuenta(:|=)(\\t|\\r|\\n|\s)*({domain}.+?)(\\t|\\r|\\n|\s)*Id. de inicio de sesión(:|=)""",
  """\s*Nombre de cuenta(:|=)(\\t|\\r|\\n|\s)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\s)*""",
  """Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s|;)""",
  """Estación de trabajo de origen:(\\t|\\r|\\n|\s)*({src_host}[\w\-\.]+)(\\t|\\r|\\n|\s)*"""
]
ParserVersion = "v1.0.0"

spanish-windows-events = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Fields = [
	  """Message=({event_name}[^\.]+)""",
	  """({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""",
	  """Keywords=({result}.+?);?(\\t|\\r|\\n|\s)*Message=""",
	  """EventCode=({event_code}\d+)""",
	  """Nombre de proceso(:|=)(\\t|\\r|\\n|\s)*({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))\s(\\t|\\r|\\n|\s)*""",
	  """\s*Id. de inicio de sesión(:|=)(\\t|\\r|\\n|\s)*({login_id}[^\s]+)""",
	  """\s*Servidor(:|=)(\\t|\\r|\\n|\s)*({object_server}.+?)(\\t|\\r|\\n|\s)*Nombre de servicio""",
	  """\s*Privilegios(:|=)(\\t|\\r|\\n|\s)*({privileges}.+?)(\s*$|\s+\d+|"|,|;)"""
	  """TaskCategory=({service_type}[^=]+?)(\\t|\\r|\\n|\s)*(;|\w+=|$)"""
	  """RecordNumber=\s*({event_id}\d+)"""
	  """Sujeto:(\\t|\\r|\\n|\s)*Id. de seguridad:(\\t|\\r|\\n|\s)*({user_sid}\S+)(\\t|\\r|\\n|\s)*"""
	  """Id. de proceso:\s*({process_id}[^\s]+)(\\t|\\r|\\n|\s)*"""
	  """Tipo de objeto:(\\t|\\r|\\n|\s)*({object_type}Key)(\\t|\\r|\\n|\s)*Nombre del objeto:\s*(-|({registry_path}[^:]+?({registry_key}[^:\\\/]+?)))(\\t|\\r|\\n|\s)*Identificador del objeto"""
	  """Información de red:(\\t|\\r|\\n|\s)*Dirección de red:(\\t|\\r|\\n|\s|\-)*Puerto:(\\t|\\r|\\n|\s|\-)*({additional_info}.+?)\.(\w+=|$|")"""
	  """Código de error:(\\t|\\r|\\n|\s)*({error_code}[^"]+)"""
  
}
```