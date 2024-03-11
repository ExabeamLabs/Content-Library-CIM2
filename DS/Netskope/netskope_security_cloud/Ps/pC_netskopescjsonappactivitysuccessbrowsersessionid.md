#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-success-browsersessionid
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [""""app": """, """"userkey": """, """"category": """, """"browser_session_id": """]
  Fields = [
    """"hostname":\s*"({src_host}[^"]+)""",
    """"timestamp":\s*({time}\d{10})""",
    """"app":\s*"\[?({app}[^"\]]+)""",
    """"url":\s*"({resource}[^"]+)""",
    """"category\s*":"({additional_info}[^"]+)""",
    """"srcip":\s*"({src_translated_ip}[A-Fa-f:\d.]+)"""",
    """"userip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"user":\s*"(unknown|(({email_address}({user}[^"@\\\/\s]+)@({domain}[^.]+)[^"]+)))"""",
    """"traffic_type":\s*"({app_type}[^"]+)""",
    """"access_method":\s*"({auth_method}[^"]+)""",
    """"activity":\s*"({operation}[^"]+)""",
    """"src_country":\s*"({country}[^"]+)""",
    """"os":\s*"((U|u)nknown|({os}[^"]+))""",
    """"browser":\s*"((U|u)nknown|({browser}[^"]+))""",
    """"page":\s*"({web_domain}[^"]+)""",
    """"url":\s*"({url}[^"]+)""",
    """"dst_location":\s*"(N/A|({domain}[^"]+))""",
    """"app":\s*"({app}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```