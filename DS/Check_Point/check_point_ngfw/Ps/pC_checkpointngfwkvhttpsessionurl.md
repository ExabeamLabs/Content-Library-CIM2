#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-http-session-url"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""" Action=""""
"""product="URL Filtering""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\-+\d+:\d\d\s+({host}\S+)\s+"""
"""\WAction="({action}[^"]+)"""
"""\Wsrc="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wappi_name="(\*+|({web_domain}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^"\/]+))""""
"""\Wmatched_category="(\*+|({category}[^"]+))""""
"""\Wweb_client_type="({user_agent}[^"]+)"""
"""\Wresource="({url}[^"]+)"""
"""\Wresource="({protocol}[^:"]+)"""
"""\Wresource="(?:[^:]+:\/+)({web_domain}[^\/:\s]+)"""
"""\Wresource="(\w+:\/+[^\/]+({uri_path}\/[^?"]+))"""
"""\Wresource="(\w+:\/+[^?]+(|({uri_query}[^"]+)))""""
"""\Wuser=".+?\(({user}[^)]+)\)"""
"""\Wsrc_user_name=".+?\(({user}[^)]+)\)"""
"""\Wsrc_machine_name="({src_host}[^@"]+)(@({domain}[^@"]+))?"""
"""\Wservice="({dest_port}\d+)"""
"""\Ws_port="({src_port}\d+)"""
"""\Wsent_bytes="({bytes_out}\d+)"""
"""\Wreceived_bytes="({bytes_in}\d+)"""
]
ParserVersion = "v1.0.0"


}
```