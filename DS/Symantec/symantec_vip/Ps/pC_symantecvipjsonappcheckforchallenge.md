#### Parser Content
```Java
{
Name = "symantec-vip-json-app-checkforchallenge"
Vendor = "Symantec"
Product = "Symantec VIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """TRANSACTION_TIMESTAMP: """""
  """ACTION_TYPE: """""
  """SUCCESS: """""
  """MESSAGE_CODE: """""
]
Fields = [
  """TRANSACTION_TIMESTAMP:\s*""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """ACTION_TYPE:\s*""({action}[^"]+)"""
  """SUCCESS:\s*""({result}[^"]+)"""
  """CLIENT_IP:\s*""({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """CLIENT_BROWSER_DATA:\s*""({user_agent}[^"]+)"""
  """CUST_LOGIN_ID:\s*""(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"


}
```