#### Parser Content
```Java
{
Name = "sophos-xgfirewall-cef-http-session-contentfiltering"
Vendor = "Sophos"
Product = "Sophos XG Firewall"
TimeFormat = "epoch"
Conditions = [
"""log_type="Content Filtering""""
""" url=""""
"""status_code"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdate=({time}\d+-\d+-\d+\s*time=\d+:\d+:\d+)"""
"""\Wdevice_name="({host}[\w\-.]+)"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wlog_subtype="({action}[^"]+)""""
"""\Wuser_name="({user}[^\s@"]+)""""
"""\Wuser_name="({email_address}[^\s@"]+@[^\s@"]+)""""
"""\Wcategory="(None|({category}[^"]+))""""
"""\Wurl="(|({url}(({protocol}[^:\\\/\s"]+):[\\\/]+)?({web_domain}[^\\\/\s:"]+)(:\d+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))""""
"""\Wsrc(_ip)?=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst(_ip)?=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\W(spt|src_port)=({src_port}\d+)"""
"""\W(dpt|dst_port)=({dest_port}\d+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wprotocol="({protocol}[^"]+)""""
"""\W(in|recv_bytes)=({bytes_in}\d+)"""
"""\W(out|sent_bytes)=({bytes_out}\d+)"""
"""\Wuser_agent\\?="({user_agent}[^"]+)""""
"""\Wstatus_code\\?="({http_response_code}\d+)"""
"""\W(dntdom|domain)=({web_domain}[^\s]+)"""
"""\W(fname|file_name)="?(|({file_name}[^"]+?))"?\s+(\w+=|$)"""
"""\Wcontenttype="({mime}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```