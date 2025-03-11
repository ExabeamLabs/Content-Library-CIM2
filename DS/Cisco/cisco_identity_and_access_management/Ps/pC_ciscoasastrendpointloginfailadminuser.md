#### Parser Content
```Java
{
Name = "cisco-asa-str-endpoint-login-fail-adminuser"
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """%AAA-5-AAA_AUTH_ADMIN_USER""", """Authentication failed for admin user""" ]
  Fields = [
  """({additional_info}Authentication failed for admin user) '({user}[\w\.\-\!\#\^\~]{1,40}\$?)' on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """%AAA-({priority}5)-({event_category}AAA_AUTH_ADMIN_USER)"""
  """aaa.c:({event_code}\d+)"""
  """\d+\.\d+\s+({host}[\w\-.]+):\s+"""
  """\s({time}\w+ \d+ \d+:\d+:\d+)"""
  ]
  ParserVersion = "v1.0.0"
  

}
```