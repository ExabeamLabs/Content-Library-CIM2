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
                """"user":"(?:|({user}[^"]+))"""",
                """"src":"(?:|({src_ip}[^"]+))"""",
                """"status":"(?:|({http_response_code}\d+))"""",
                """"protocol":"(?:|({protocol}[^"]+))"""",
                """"http_user_agent":"(?:|({user_agent}[^"]+))"""",
                """"http_method":"(?:|({method}[^"]+))"""",
                """"url":"(?:|({url}[^"]+))"""",
                """"domain_full":"(?:|({web_domain}[^"]+))"""",
                """"category":"(?:|({category}[^"]+))"""",
                """"bytes_in":"(?:|({bytes_in}\d+))"""",
                """"bytes_out":"(?:|({bytes_out}\d+))"""",
                """"cache_status":"(?:|({proxy_action}[^"]+))"""",
                """"block_reason":"(?:|({failure_reason}[^"]+))"""",
                """"dest":"(?:|({dest_ip}[^"]+))"""",
                """"dest_port":"(?:|({dest_port}\d+))"""",
                """"is_virus":"(?:|({malicious}[^"]+))"""",
                """"content_type":"(?:|({mime}[^"]+))""""
    ]
  

}
```