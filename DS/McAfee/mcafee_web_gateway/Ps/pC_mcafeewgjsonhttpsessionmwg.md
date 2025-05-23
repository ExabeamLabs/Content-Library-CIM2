#### Parser Content
```Java
{
Name = mcafee-wg-json-http-session-mwg
    Vendor = McAfee
    Product = McAfee Web Gateway
    ParserVersion = "v1.0.0"
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [""" mwg:""" ]
    Fields = [
      """\[({time}[^\]]+)""",
      """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+mwg:""",
      """\[.+?\]\s+"(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """\[.+?\]\s+".*?"\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+({http_response_code}\d+)""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"({method}[^\s]+)""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+(({protocol}\w+):\/+)?""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+({url}\S+)""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\/:]+))""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+(\w+:\/+)?[^\/:]+:({dest_port}\d+)""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+(\w+:\/+)?[^\/:]+(:\d+)?({uri_path}\/.*?)(\?|\s+[^\s]+")""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+(\w+:\/+)?[^\/:]+(:\d+)?\/[^?]+({uri_query}\?.*?)\s+[^\s]+"""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+".*?"\s+"(?:-|({category}[^,"]+))""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){3}"(?:|({mime}[^"]+))"""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){4}"(?:|({user_agent}[^"]+))"""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){6}\d+\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){6}([^\s]+\s+){2}({bytes_in}\d+)""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){6}([^\s]+\s+){3}({bytes_out}\d+)""",
      """\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){6}([^\s]+\s+){6}"(?:|({failure_reason}[^"]+))"""",
    ]
  

}
```