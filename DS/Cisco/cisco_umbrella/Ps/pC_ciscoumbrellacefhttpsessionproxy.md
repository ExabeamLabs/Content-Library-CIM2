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
    """\Wsuser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """"contentTpe"+:"+({mime}[^",]+)""",
    """"externalIp":"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"internalIp":"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"destinationIp"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"responseSize"+:"+({bytes_out}\d+)"""",
    """"requestSize"+:"+({bytes_in}\d+)"""",
    """"statusCode"+:"+({http_response_code}\d+)"""",
    """"timestamp"+:"+({time}[^",]+)"""",
    """"referer"+:"+({referrer}[^",]+)"""",
    """"userAgent"+:"+(\s+|({user_agent}[^"]+))","""",
    """"url"+:"+(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[^\\\/\s:,"]+))?(:({dest_port}\d+))?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))"""",
    """"url"+:"+({protocol}http(s)?)""",
    """"sha"+:"+({sha}[^",]+)"""",
    """"categories":\[({categories}"({category}[^",]+?)"[^\]]*?)\]""",
    """"verdict"+:"+({action}[^",]+)""",
    """"identityType"+:"+({identity_type}[^",]+)""",
    """"identities"+:\["+({dest_host}[\w-]+)\.?""",
    """"identities"+:\["+\s*({full_name}[^"\(]+).+?\('?({email_address}({user}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+)@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|\)']+))"""
    """"identities":\[("({dest_host}[\w\-\.]+)")?,"({full_name}[^\("]+?)(?:\s*\(\w+}\)\s*)?(\s+\(({email_address}(({user}[A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9])+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))""""
  ]


}
```