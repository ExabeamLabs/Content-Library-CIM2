#### Parser Content
```Java
{
Name = "apache-guacamole-str-app-authentication-success-user"
Vendor = "Apache"
Product = "Apache Guacamole"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """auth.AuthenticationService - User"""
  """] INFO """
  """successfully authenticated from """
]
Fields = [
  """User \"{1,20}({user}[\w\.\-]{1,40}\$?)\"{1,20} successfully authenticated from"""
  """successfully authenticated from\s\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]"""
]
ParserVersion = "v1.0.0"


}
```