#### Parser Content
```Java
{
Name = ibm-guardium-csv-database-login-fail-loginfailed
Vendor = "IBM"
Product = "Infosphere Guardium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  ""","LOGIN_FAILED","""
]
Fields = [
  """([^,]*,){7}"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """([^,]*,){2}"({session_id}[^,"]*)""""
  """([^,]*,){3}"({user}[^,"]*)""""
  """([^,]*,){4}"({src_ip}[a-fA-Z:\d.]*)""""
  """([^,]*,){5}"({dest_ip}[a-fA-Z:\d.]*)""""
  """([^,]*,){6}"({server_group}[^,"]*)""""
  """([^,]*,){8}"({failure_reason}[^,"]*)""""
  """\Wreason\s*-\s*({failure_reason}[^,"]*)""""
  """([^,]*,){11}"({exception_type}[^,"]*)""""
  """([^,]*,){12}"({additional_info}[^,"]*)""""
]
ParserVersion = "v1.0.0"


}
```