#### Parser Content
```Java
{
Name = "zeek-z-json-endpoint-authentication-success-kerberos"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """kerberos.log"""
  """"id.orig_h":"""
  """"id.resp_h":"""
]
Fields = [
  """"HOST\"+:\s*\"+({host}[^\"]+)""""
  """"TAGS\"+:\s*\"+({event_code}[^\"]+)\""""
  """"ts\\?\"+:\\?\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
  """"client\\?\"+:\\?\"+({user}[^\"\\]+)"""
  """"id\.orig_h\\?\"+:\\?\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"id\.orig_p\\?\"+:({src_port}\d+)"""
  """"id\.resp_h\\?\"+:\\?\"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"id\.resp_p\\?\"+:({dest_port}\d+)"""
  """"request_type\\?\"+:\\?\"+({request_type}[^\"\\]+)"""
  """"client\\?\"+:\\?\"+({user}[^\"\/\\]+)(\/({domain}[^\"\\]+))?"""
  """"service\\?\"+:\\?\"+({service_name}[^\"\/\\@]+)"""
  """"success\\?\"+:({result}\w+)"""
  """"error_msg\\?\"+:\\?\"+({result_code}[^\"\\]+)"""
  """"cipher\\?\"+:\\?\"+({ticket_encryption_type}[^\"\\]+)"""
]
ParserVersion = "v1.0.0"


}
```