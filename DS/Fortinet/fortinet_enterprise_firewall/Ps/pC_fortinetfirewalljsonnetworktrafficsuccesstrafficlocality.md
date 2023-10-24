#### Parser Content
```Java
{
Name = "fortinet-firewall-json-network-traffic-success-trafficlocality"
Vendor = "Fortinet"
Product = "Fortinet Enterprise Firewall"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""first_switched"""
"""traffic_locality"""
]
Fields = [
"""\Wip_protocol"*:"*\s*({protocol}[^",]*?)\s*("|,)"""
"""\Whost"*:"*\s*({host}[\w\-.]*)"""
"""\Wsrc_addr"*:"*\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsrc_port"*:\s*(([A-Fa-f:\d.]+?):)?({src_port}\d+)?\s*("|,|$)"""
"""\Wdst_addr"*:"*\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdst_port"*:\s*(([A-Fa-f:\d.]+?):)?({dest_port}\d+)?\s*("|,|$)"""
"""\Wdirection"*:"*\s*({direction}[^",]*?)\s*("|,)"""
"""("|:)({time}\d\d\d\d-\d\d-\d\d(T|\s+)\d\d:\d\d:\d\d)"""
"""\Wbytes"*:\s*({bytes}\d+)"""
"""\Wservice_name"*:"*\s*({service_name}[^("\s]*)"""
"""\Wflow_end_reason"*:\s*({end_reason}\d+)"""
"""\Wfirst_switched"*:"*\s*({time_start}[^",]*?)\s*("|,)"""
"""\Wlast_switched"*:"*\s*({time_end}[^",]*?)\s*("|,)"""
"""\Wpackets"*:\s*({packets}\d+)"""
"""\Wtraffic_locality"*:"*\s*(|({locality}[^",]*?))\s*("|,|$)"""
""""src_hostname":"({src_host}[^"]+)""",
"""\Wtz="?({tz}[+-]\d+)"""
]
ParserVersion = "v1.0.0"


}
```