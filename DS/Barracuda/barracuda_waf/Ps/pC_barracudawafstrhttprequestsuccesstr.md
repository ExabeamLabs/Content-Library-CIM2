#### Parser Content
```Java
{
Name = barracuda-waf-str-http-request-success-tr
    ParserVersion = v1.0.0
    Vendor = Barracuda
    Product = Barracuda WAF
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
    Conditions = [ """ barracuda """ ,""" TR """ ]
    Fields = [
      """ barracuda ({time}\d{4}\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d+ (\-|\+)\d+) barracuda TR """,
# log_type_code is removed
# unit_name is removed
# service_ip is removed
      """ barracuda TR ([^\s]+\s+){2}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+({src_port}\d+)""",
      """ barracuda TR ([^\s]+\s+){4}"(?:-|({login_id}[^"]+))"""",
# certificate_user is removed
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}(?:-|({method}[^\s]+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}[^\s]+\s+(?:-|({protocol}[^\s]+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){2}(?:-|({web_domain}[^\s]+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){2}({top_domain}(?!(?:\d+\.){3}\d+)[^\.\s\/:]+(?=(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+(\s|\/|$))[^\s\/]+)""",
      
# protocol_version is removed
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){4}(?:-|({http_response_code}\d+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){5}(?:-|({bytes_out}\d+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){6}(?:-|({bytes_in}\d+))""",
# cache_hit is removed
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){8}(?:-|({time_taken}\d+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){9}(?:-|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){10}(?:-|({dest_port}\d+))""",
# server_time is removed
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"(?:-|({session_id}[^"]+))"""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+(?:-|({response_type}[^\s]+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+[^\s]+\s+(?:-|({profile}[^\s]+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){2}(?:-|({connection_type}[^\s]+))""",
      # wf_match is removed    
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){4}(?:-|({uri_path}[^\s]+))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"(?:-|({uri_query}[^"]+))"""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"[^"]+"\s+(?:-|({referrer}[^\s]+))""",
      # cookie is removed
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"[^"]+"\s+[^\s]+\s+.+?\s+"(?:-|({user_agent}[^"]+))"""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"[^"]+"\s+[^\s]+\s+.+?\s+"(?:-|Mozilla\/.+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"[^"]+"\s+[^\s]+\s+.+?\s+"[^"]+"\s+(?:-|({proxy_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
# proxy_port is removed
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"[^"]+"\s+[^\s]+\s+.+?\s+"[^"]+"\s+([^\s]+\s+){2}"(?:-|({user}[^"]+))"""",
      """ barracuda TR ([^\s]+\s+){4}("[^"]+"\s+){2}([^\s]+\s+){12}"[^"]+"\s+([^\s]+\s+){5}"[^"]+"\s+[^\s]+\s+.+?\s+"[^"]+"\s+([^\s]+\s+){2}("[^"]+"\s+){4}(?:-|({request_id}[^\s]+))\s*$"""
    ]
  

}
```