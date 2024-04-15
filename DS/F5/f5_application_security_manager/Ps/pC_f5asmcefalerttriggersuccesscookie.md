#### Parser Content
```Java
{
Name = "f5-asm-cef-alert-trigger-success-cookie"
Vendor = "F5"
Product = "F5 Application Security Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ASM:"""
  """HTTP"""
  """Cookie:"""
]
Fields = [
  """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+(\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({dest_host}[^\s]+)\s+)?ASM:"""
  """\sASM:(\"[^\"]*\",)\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """\sASM:(\"[^\"]*\",){2}\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sASM:(\"[^\"]*\",){3}\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """\sASM:(\"[^\"]*\",){5}\"({protocol}[^\"]+)""""
  """\sASM:(\"[^\"]*\",){8}\"({additional_info}[^\"]+)""""
  """\sASM:(\"[^\"]*\",){8}\"({alert_name}[^\"]+)""""
  """\sASM:\"({alert_name}[^\"]+)""""
  """\sASM:(\"[^\"]*\",){9}\"(?:N\/A|({user}[^\"]+))""""
  """\sASM:(\"[^\"]*\",){13}\"\w+\s+({malware_url}[^\"]+?)(?:\s+\w+\/\d\.\d|)((\\r\\n|\s+)[\w\-]+:|\")"""
  """(\\r\\n|\s)Host:\s*({domain}[^\"]+?)((\\r\\n|\s+)[\w\-]+:|\")"""
  """(\\r\\n|\s)User-Agent:\s*({user_agent}[^\"]+?)(\\r\\n[\w\-]+:|\")"""
]
DupFields = [
  "protocol->alert_type"
]
ParserVersion = "v1.0.0"


}
```