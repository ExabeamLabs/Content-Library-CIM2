#### Parser Content
```Java
{
Name = imanage-i-json-app-activity-success-checkout
Vendor = iManage
Product = iManage
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"docnum":"""
  """"activity":"""
  """"docname":"""
  """"docsize":"""
]
Fields = [
  """"activity_datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """"employee_cms_code":"(UNKNOWN|({user_id}[^"]+))"""
  """"location":"(UNKNOWN|({src_ip}(\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]*:[A-Fa-f\d:]+)|({src_host}[^"]+))""""
  """"docnum":(UNKNOWN|({resource}[^,"]+))"""
  """"fullname":"(UNKNOWN|({full_name}[^"]+))"""
  """"activity":"(UNKNOWN|({operation}[^"]+))"""
  """"database":"(UNKNOWN|({app}[^"]+))"""
  """"docname":"(UNKNOWN|({object}[^"]+?))\s*""""
  """"client_code":"(UNKNOWN|({client_id}[^"]+))"""
  """"email":"({email_address}[^@"]+@[^"]+)""""
  """"docuser":"({user}[^"]+)""""
  """"appname":"({app}[^"]+)""""
  """"docloc":"({file_path}({file_dir}([^"]+)?[\/\\])?({file_name}[^\/\\"]+))""""
]
ParserVersion = "v1.0.0"
},	 

{
Vendor = Imprivata
Product = Imprivata
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """\d\d:\d\d:\d\d ({host}[\w\-.]+) ({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """ServerIP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """User:\s*({user}[^\s\#]+)"""
  """Event:\s*({operation}.+?)\s+ServerIP:"""
  """({app}Imprivata)"""
]
Name = imprivata-i-kv-app-activity-success-agentshutdown
Conditions = [
  """Event: Agent Shutdown"""
]
ParserVersion = "v1.0.0"


}
```