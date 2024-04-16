#### Parser Content
```Java
{
Name = "mcafee-wg-kv-http-session-fail-accesdenied"
    Vendor = McAfee
    Product = McAfee Web Gateway
	ParserVersion = "v1.0.0"
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """mwg: Acces Denied [""" ]
    Fields = [
      """\s+({host}[^\s]+)\s+mwg:""",
      """({failure_reason}Acces Denied)""",
      """mwg:\s+Acces Denied\s+\[({time}[^\]]+)\]""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+".*?"\s+"(?:|-|({user}[\w\.\-]{1,40}\$?))"""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+(".*?"\s+){2}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+(".*?"\s+){2}[^\s]+\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"(?:"|-"|({web_domain}[^\s"]+)")""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+({http_response_code}\d+)""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+({bytes_out}\d+)""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+\d+\s+({bytes_in}\d+)""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}"({method}[^\s]+)""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}"\w+\s+(?:({protocol}\w+):\/+)?""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}"\w+\s+(\w+:\/+)?[^\/:]+:({dest_port}\d+)""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}"\w+\s+({url}\S+)""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}"\w+\s+(\w+:\/+)?[^\/:]+(:\d+)?({uri_path}\/.*?)(\?|\s+[^\s]+")""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}"\w+\s+(\w+:\/+)?[^\/:]+(:\d+)?\/[^?]+({uri_query}\?.*?)\s+[^\s]+"""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}("[^"]*?"\s+){3}\d+\s+"(?:-|({category}[^,"]+))"""
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}("[^"]*?"\s+){3}\d+\s+"[^"]*?"\s+\d+\s+"(?:-|({action}[^"]+))"""",
      """mwg:\s+Acces Denied\s+\[.+?\]\s+("[^"]*?"\s+){2}([^\s]+\s+){2}"[^"]*?"\s+\d+\s+"[^"]*?"\s+(\d+\s+){2}("[^"]*?"\s+){3}\d+\s+"[^"]*?"\s+(\w+\s+"[^"]*?"\s+){3}("[^"]*?"\s+){2}"(?:|-|({user_agent}[^"]+?)\s*)("|$)"""
    ]
  

}
```