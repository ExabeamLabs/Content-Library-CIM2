#### Parser Content
```Java
{
Name = ibm-guardium-csv-database-login-success-no
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """","\N","1""""
  """","No""""
]
Fields = [
  """([^,]*,){7}"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """([^,]*,){1}"({session_id}[^,"]*)""""
  """([^,]*,){5}"({db_name}[^,"]*)""""
  """([^,]*,){8}"(({domain}[^\\",]+)\\+)?({db_user}[^\\,"]*)""""
  """([^,]*,){9}"(({domain}[^\\",]+)\\+)?({user}[^\\,"]*)""""
  """([^,]*,){10}"({process_name}[^,"]*)""""
  """([^,]*,){11}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """([^,]*,){12}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """([^,]*,){13}"({service_name}[^,"]*)""""
  """([^,]*,){14}"({src_host}[\w\-.]*)""""
  """([^,]*,){15}"({server_group}[^,"]*)""""
  """([^,]*,){16}"({dest_host}[\w\-.]*)""""
  """([^,]*,){19}"({protocol}[^,"]*)""""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```