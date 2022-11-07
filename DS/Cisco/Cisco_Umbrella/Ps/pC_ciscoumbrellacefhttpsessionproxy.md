#### Parser Content
```Java
{
Name = cisco-umbrella-cef-http-session-proxy
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """destinationServiceName =Cisco Umbrella """, """dproc=Proxy """, """"url":""" ]
  Fields = [
    """\W(destinationServiceName|requestClientApplication)=({app}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wsuser=(anonymous|({user}[^=]+?))(\s+\w+=|\s*$)""",
    """"contentTpe"+:"+({mime}[^",]+)""",
    """"externalIp":"+({dest_ip}[a-fA-F\d.:]+)""",
    """"internalIp":"+({src_ip}[a-fA-F\d.:]+)""",
    """"destinationIp"+:"+({dest_ip}[^",]+)"""",
    """"responseSize"+:"+({bytes_out}\d+)"""",
    """"requestSize"+:"+({bytes_in}\d+)"""",
    """"statusCode"+:"+({http_response_code}\d+)"""",
    """"timestamp"+:"+({time}[^",]+)"""",
    """"referer"+:"+({referrer}[^",]+)"""",
    """"userAgent"+:"+(\s+|({user_agent}[^"]+))"""",
    """"url"+:"+(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\\\/\s:,"]+))?(:({dest_port}\d+))?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))"""",
    """"url"+:"+({protocol}http(s)?)""",
    """"sha"+:"+({sha}[^",]+)"""",
    """"categories"+:\["+({category}[^",]+)""",
    """"verdict"+:"+({action}[^",]+)""",
    """"identityType"+:"+({identity_type}[^",]+)""",
    """"identities"+:\["+({dest_host}[\w-]+)\.""",
    """"identities"+:\["+({full_name}.+?)\s*\(({email_address}({user}[^@]+)@[^\)"]+)"""
    """"categories"+:\["+({categories}[^"]+)"""",
  ]


}
```