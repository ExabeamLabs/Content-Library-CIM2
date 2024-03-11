#### Parser Content
```Java
{
Name = symantec-endpointprotection-csv-network-traffic-fail-bloques
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ SymantecServer: """, """IP de l’hôte local""", """Action""", """ Bloqués""" ]
  Fields = [
  """SymantecServer: ({host}({src_host}[\w\-\.]+)),""",
  """IP de l’hôte local :\s({src_ip}((([0-9a-fA-F.:]{1,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """Port local :\s({src_port}\d{1,5}),""",
  """Adresse IP de l’hôte distant :\s({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """Nom de l’hôte distant :\s(|({dest_host}[\w\-\.]+))""",
  """Port distant :\s({dest_port}\d{1,5}),""",
  """Port distant :[^,]+,({direction}[^,]+),""",
  """Action :\s({action}Bloqués)""",
  """Application :\s({process_path}(({process_dir}[^",]+?)[\/\\]+)?({process_name}[^\/\\",]+?)),Action"""
  ]
 

}
```