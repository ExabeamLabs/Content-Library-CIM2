#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-detecte
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """SymantecServer""", """Source : Analyse""", """détecté""", """Action secondaire :""", """Jeu de catégories : Malware""" ]
  Fields = [
  """événement\s:\s({time}\d{4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})"""
  """SymantecServer:\s({event_name}[^,]+),Adresse IP :"""
  """Adresse IP\s:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Nom du risque\s:\s({alert_name}[^,]+)"""
  """Chemin de fichier :\s({process_path}(({process_dir}\w+:[^,]+)[\\]+)?({process_name}[^\\.]+\.[^\"\\,:]+))"""
  """Action réelle\s:\s({action}[^,]+)"""
  """Nom du serveur\s:\s({host}[\w\-.]+)"""
  """Nom d’utilisateur\s:\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Hachage d’application :\s({hash_md5}[^,]+)"""
  """Jeu de catégories :\s({alert_type}[^,]+)"""
  """Type de catégorie :\s({additional_info}[^,]+)"""
 ]	


}
```