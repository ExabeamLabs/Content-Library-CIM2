#### Parser Content
```Java
{
Name = ibm-guardium-csv-database-login-fail-loginfailed
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  ""","LOGIN_FAILED","""
]
Fields = [
  """([^,]*,){7}"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """([^,]*,){2}"({session_id}[^,"]*)""""
  """([^,]*,){3}"({user}[^,"]*)""""
  """([^,]*,){4}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """([^,]*,){5}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """([^,]*,){6}"({server_group}[^,"]*)""""
  """([^,]*,){8}"({result_reason}[^,"]*)""""
  """\Wreason\s*-\s*({result_reason}[^,"]*)""""
  """([^,]*,){11}"({exception_type}[^,"]*)""""
  """([^,]*,){12}"({additional_info}[^,"]*)""""
]
ParserVersion = "v1.0.0"


}
```