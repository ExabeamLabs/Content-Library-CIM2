#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-http-session-filtering"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "epoch_sec"
Conditions = [
"""|loguid="""
"""|origin="""
"""|product="""
"""product=URL Filtering"""
]
Fields = [
"""time=({time}\d{10})\|"""
"""hostname=({host}[^|]+)\|"""
"""app_category=({category}[^|]+)\|"""
"""appi_name=({app}[^|]+)\|"""
"""layer_uuid=({user_uid}[^|]+)\|"""
"""rule_action=({action}[^|]+)\|"""
"""\|action=({action}[^\|]+)"""
"""rule_name=({rule}[^\|]+)\s*\|"""
"""origin=({origin_ip}[^|]+)\|"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|"""
"""method=({method}[^|]+)\|"""
"""\|resource=((https|http)?:\/+)({web_domain}([^:\|\/]+))"""
"""service=({dest_port}\d+)\|"""
"""service_id=({protocol}[^|]+)\|"""
"""protocol=({protocol}[^\|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|"""
"""conn_direction=({direction}[^|]+)\|"""
"""ifname=({src_interface}[^|]+)\|"""
"""\|bytes=({bytes}\d+)"""
"""\|server_inbound_bytes=({bytes_in}\d+)"""
"""\|server_outbound_bytes=({bytes_out}\d+)"""
"""(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"


}
```