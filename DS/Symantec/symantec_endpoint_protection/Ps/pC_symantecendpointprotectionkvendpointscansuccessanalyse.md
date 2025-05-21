#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-endpoint-scan-success-analyse
Vendor = Symantec
Product = Symantec Endpoint Protection
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """SymantecServer: """, """ID de l’analyse :""", """Type d’analyse : Analyse planifiée""", """Utilisateur1 :""" ]
Fields = [
  """Commencer[^:]*:\s({time}\d{4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})""",
  """Adresse IP[^:]*:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """Ordinateur[^:]*:\s({src_host}[\w\-.]+)""",
  """Nom du domaine[^:]*:\s({src_domain}[^,]+)""",
  """Nom du serveur[^:]*:\s({host}[^,]+)""",
  """Utilisateur1[^:]*:\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  """Utilisateur2[^:]*:\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  """Type d’analyse[^:]*:\s({event_name}Analyse planifiée)""",
  """Utilisateur2[^:]*:\s[^,]+,({additional_info}[^=]+?),Ordinateur"""
]


}
```