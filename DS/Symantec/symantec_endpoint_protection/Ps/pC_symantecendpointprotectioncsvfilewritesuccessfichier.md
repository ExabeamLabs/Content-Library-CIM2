#### Parser Content
```Java
{
Name = symantec-endpointprotection-csv-file-write-success-fichier
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,Commencer :""", """,Type d’action :""", """,ID du périphérique :""", """,Taille de fichier""" ]
  Fields = [
  """SymantecServer:\s({host}[\w\-.]+)""",
  """(0.0.0.0|({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))|({src_host}[^\s,]+)),Bloqués,""",
  """Commencer :\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """Règle : [^,]*,\d+,({target}[^,]+),""",
  """Règle : [^,]*,\d+,({process_path}({process_dir}[^"]*?)(\/|\\)({process_name}[^\/\\]+)),\d,""",
  """,({file_path}(({file_dir}[^,]*)[\/\\])[^,]+),Nom d’utilisateur"""
  """,[^",]+[\\\/]({file_name}[^,]*?(\.({file_ext}[^,]+))?),Nom d’utilisateur""",
  """\| \[[^,]*,\d+,[^,]+,\d+,[^,]+,[^",]*/({file_name}[^",]+?(\.({file_ext}[^,"\s\.]+))?)"?,Nom d’utilisateur""",
  """Nom d’utilisateur :\s+(SYSTEM|Système|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\(\w+\))?,Nom du domaine :""",
  """Nom du domaine :\s+(|AUTORITE NT|({domain}[^:,]+?)),Type d’action :""",
  """Taille de fichier \(({bytes_unit}[^\)]+?)\) :\s*({bytes}\d+)""",
  """ID du périphérique :\s+({device_id}[^"]+)&\d+""",
  """SymantecServer:\s([^,]*,){2}({result}[^,]+),"""
  ]
  DupFields = ["result->operation"]


}
```