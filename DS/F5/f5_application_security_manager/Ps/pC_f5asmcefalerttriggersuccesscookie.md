#### Parser Content
```Java
{
Name = "f5-asm-cef-alert-trigger-success-cookie"
Vendor = "F5"
Product = "F5 Application Security Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ASM:"""
  """"HTTP"""
  """Cookie:"""
]
Fields = [
  """\w+\s\d+\s\d+:\d+:\d+\s({host}[\w\.]+)\sASM:"""
  """\sASM:(\"[^\"]*\",)\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """\sASM:(\"[^\"]*\",){2}\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sASM:(\"[^\"]*\",){3}\"({dest_port}\d+)"""
  """\sASM:(\"[^\"]*\",){3}\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """\sASM:(\"[^\"]*\",){8}\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """\sASM:(\"[^\"]*\",){12}\"({method}[^"]+)"""
  """\sASM:(\"[^\"]*\",){5}\"({protocol}[^\"]+)""""
  """\sASM:(\"[^\"]*\",){15}\"({protocol}[^\"]+)""""
  """\sASM:(\"[^\"]*\",){17}\"({additional_info}[\S\s]+(?:\\r\\n\\r\\n))\",\"\w+"""
  """\sASM:(\"[^\"]*\",){8}\"({alert_name}(?!\d+(?:\.\d+){3})[^"]+)"""
  """\sASM:\"({result_reason}[^\"]+)""""
  """\sASM:(\"[^\"]*\",){8}"([\w\s\,\/\-]+)","({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """\sASM:(\"[^\"]*\",){13}\"\w+\s+({malware_url}[^\"]+?)(?:\s+\w+\/\d\.\d|)((\\r\\n|\s+)[\w\-]+:|\")"""
  """(\\r\\n|\s)Host:\s*({web_domain}[\w\-\.]+?)((\\r\\n|\s+)[\w\-]+:|\")"""
  """(\\r\\n|\s)User-Agent:\s*({user_agent}[^\"]+?)(\\r\\n[\w\-]+:|\")"""
  """(\\r\\n|\s)Referer:\s*({referrer}[^"]+?)((\\r\\n|\s+)[\w\-]+:|\")"""
  """(\\r\\n|\s)X-Forwarded-For:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\r\\n\\r\\n|\s+)"""
  """(\d+\.){3}\d+\\r\\n\\r\\n\",\"({action}[^"]+)"""
  """(?:\\r\\n|\s)X-Forwarded-For:\s*(?:\d+\.){3}\d+\\r\\n\\r\\n\",(?:"[^"]+",){5}\"({severity}[^"]+)"""
  """\<\/html\>\\r\\n\",(?:\"[^"]+\",){3}\"({severity}[^"]+)"""
  """<viol_name>({alert_name}[^<]+)<\/viol_name>"""
]
DupFields = [
  "protocol->alert_type"
]
ParserVersion = "v1.0.0"


}
```