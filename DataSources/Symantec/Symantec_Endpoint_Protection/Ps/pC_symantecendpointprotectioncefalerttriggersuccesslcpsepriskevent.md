#### Parser Content
```Java
{
Name = symantec-endpointprotection-cef-alert-trigger-success-lcpsepriskevent
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""CEF:"""
"""|Symantec|"""
"""|lcp_sep_risk_event|"""
]
Fields = [
"""({host}[\w.\-]+)\s+lcp_sep_risk_event:"""
"""CEF:([^\|]*\|){5}({alert_type}[^\|]+)"""
"""\"device_time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""\WinternalIP=({src_ip}[a-fA-F\d.:]+)"""
"""\WinternalHost=({src_host}[^=]+?)(\s+\w+=|\s*$)"""
"""\Wmd5=({hash_md5}[^=]+?)(\s+\w+=|\s*$)"""
"""\Wuser_name=({user}[^=]+?)(\s+\w+=|\s*$)"""
"""\Wdomain_name=({domain}[^=]+?)(\s+\w+=|\s*$)"""
"""\"app_name\":\"({process_path}({process_dir}[^\"]*?)({process_name}[^\"\\\/]+))\""""
"""\"event_desc\":\"({additional_info}[^\"]+)"""
"""\"severity\":({alert_severity}\d+)"""
"""\"signature_name\":\"({alert_name}[^\"]+)"""
"""external_ip":"({dest_ip}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```