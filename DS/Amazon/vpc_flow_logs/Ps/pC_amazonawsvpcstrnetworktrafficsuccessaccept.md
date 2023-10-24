#### Parser Content
```Java
{
Name = "amazon-awsvpc-str-network-traffic-success-accept"
ParserVersion = v1.0.0
Vendor = "Amazon"
Product = "VPC Flow Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
flow_start_timeFormat = ["epoch_sec"]
flow_end_timeFormat = ["epoch_sec"]
Conditions = [ """ACCEPT""" , """vpc-""" ]
Fields = [
"""({account_id}\d+)\s+ACCEPT"""
"""({action}ACCEPT)"""
"""ACCEPT(?:\s[^\s]+){1}\s({bytes}\d+)"""
"""ACCEPT(?:\s[^\s]+){2}\s(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*"""
"""ACCEPT(?:\s[^\s]+){3}\s({dest_port}\d+)"""
"""ACCEPT(?:\s[^\s]+){4}\s({flow_end_time}\d+)"""
"""ACCEPT(?:\s[^\s]+){5}\s({direction}\S+)"""
"""ACCEPT(?:\s[^\s]+){6}\s({instance_id}[^\s]+)"""
"""ACCEPT(?:\s[^\s]+){7}\s({interface_id}[^\s]+)"""
"""ACCEPT(?:\s[^\s]+){8}\s({status_msg}[^\s]+)"""
"""ACCEPT(?:\s[^\s]+){9}\s({packets}\d+)"""
"""({protocol}\d+)(?:\s[^\s]+){11}\svpc-"""
"""({region}[^\s]+)(?:\s[^\s]+){10}\svpc-"""
"""(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(?:\s[^\s]+){9}\svpc-"""
"""({src_port}\d+)(?:\s[^\s]+){8}\svpc-"""
"""({flow_start_time}\d+)(?:\s[^\s]+){7}\svpc-"""
"""({tcp_flags}\S+)(?:\s[^\s]+){3}\svpc-"""
"""({vpc}vpc-[^\s]+)"""
"""host\*":\*"({src_host}[\w\-\.]+)"""
"""protocol\*":\*"({protocol}[\w\-\.]+)"""
]


}
```