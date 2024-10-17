#### Parser Content
```Java
{
Name = mcafee-wg-json-http-session-sha256
    Vendor = McAfee
    Product = McAfee Web Gateway
    ParserVersion = "v1.0.0"
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """"file_sha256_hash":""",""""domain_full":""","""mwg:"""]
    Fields = [
                """"timestamp":"\[({time}[^\]]+)""",
                """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+mwg:""",
                """"user":"(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
                """"src":"(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
                """"status":"(?:|({http_response_code}\d+))"""",
                """"protocol":"(?:|({protocol}[^"]+))"""",
                """"http_user_agent":"(?:|({user_agent}[^"]+))"""",
                """"http_method":"(?:|({method}[^"]+))"""",
                """"url":"(?:|({url}[^"]+))"""",
                """"domain_full":"(?:|({web_domain}[^"]+))"""",
                """"category":"(-|none|({categories}({category}[^",;:]+)[^"]*))"""",
                """"bytes_in":"(?:|({bytes_in}\d+))"""",
                """"bytes_out":"(?:|({bytes_out}\d+))"""",
                """"cache_status":"(?:|({proxy_action}[^"]+))"""",
                """"block_reason":"(?:|({failure_reason}[^"]+))"""",
                """"dest":"(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
                """"dest_port":"(?:|({dest_port}\d+))"""",
                """"is_virus":"(?:|({result}[^"]+))"""",
                """"content_type":"(?:|({mime}[^"]+))""""
    ]
  

}
```