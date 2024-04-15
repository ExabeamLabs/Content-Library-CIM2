#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-lognetworkvirus"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""[LogNetworkVirus"""
"""Network Virus Name ="""
"""Victim IP="""
]
Fields = [
"""\d+ ({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""Network Virus Name ="({alert_name}[^"]+)""""
"""Domain="({domain}[^"]+)"""
"""User="({user}[^"]+)"""
"""Attacker IP="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""Device name="({src_host}[^"]+)"""
"""Victim IP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"alert_name->alert_type"
"src_host->host"
]
ParserVersion = "v1.0.0"


}
```