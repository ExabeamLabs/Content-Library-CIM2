#### Parser Content
```Java
{
Name = "zeek-z-json-endpoint-login-id"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """"id.orig_h":"""
  """"id.resp_h":"""
  """"kerberos","""
]
Fields = [
  """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
  """"uid":"({connection_id}[^"]+)"""
  """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"id\.orig_p":({src_port}\d+)"""
  """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"id\.resp_p":({dest_port}\d+)"""
  """"client":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\/({domain}[^"]+)""""
  """"service":"({service_name}[^"]+)"""
  """"success":({result}[^,]+)"""
  """"error_msg":"({result_code}[^"]+)"""
  """"cipher":"({ticket_encryption_type}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```