#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-alertname
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type": """, """"alert": "yes"""", """"alert_name":"""]
  Fields = [
    """"timestamp":\s*({time}\d{10})""",
    """"hostname":\s*"({dest_host}[^"]+)""",
    """"policy":\s*"({alert_name}[^"]+)"""",
    """"alert_type":\s*"({alert_type}[^"]+)"""",
    """"dstip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"url":\s*"({malware_url}[^"]+)"""",
    """"alert_name":\s*"({alert_name}[^"]+)"""",
    """"internal_id":\s*"({alert_id}[^"]+)"""",
    """"category\s*":"({additional_info}[^"]+)""",
    """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"user"+:\s*"+(unknown|(({email_address}[^"@\\\/\s]+@({domain}[^.]+)[^"]+)))"""",
    """"activity":\s*"({operation}[^"]+)""",
    """"src_country":\s*"({country}[^"]+)""",
    """"os":\s*"((U|u)nknown|({os}[^"]+))""",
    """"browser":\s*"((U|u)nknown|({browser}[^"]+))""",
    """"page":\s*"({web_domain}[^"//]+)""",
    """"dst_location":\s*"(N/A|({location}[^"]+))""",
    """"app":\s*"({app}[^"]+)""",
    """"md5":\s*"({hash_md5}[^"]+)"""",
    """"from_user":\s*"({from_user_at}[^"]+)"""",
    """"file_path":\s*"({file_path_at}[^"]+)"""",
    """"shared_with":\s*"({shared_with_at}[^"]+)"""",
    """"site":\s*"({site_at}[^"]+)""""
    """"protocol":\s*"({protocol}[^"]+)""""
    """"domain":\s*"([^"]+\.)({top_domain}[^\."]+\.[^\."]+)""""
    """"file_size":\s*({bytes}\d+)"""
    """"domain":"({domain}[^"]+)""""
  ]
  DupFields = [
"alert_name"->"alert_subject"
]


}
```