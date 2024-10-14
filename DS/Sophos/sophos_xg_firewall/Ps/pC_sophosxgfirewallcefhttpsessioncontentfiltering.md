#### Parser Content
```Java
{
Name = "sophos-xgfirewall-cef-http-session-contentfiltering"
Vendor = "Sophos"
Product = "Sophos XG Firewall"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","epoch","yyyy-MM-dd' time='HH:mm:ss"]
Conditions = [
""" log_type="Content Filtering""""
""" url=""""
""" log_component="HTTP"""
]
Fields = [
"""timestamp="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(\+|\-)[\d:]+)"""
"""\Wrt=({time}\d{13})"""
"""\Wdate=({time}\d+-\d+-\d+\s*time=\d+:\d+:\d+)"""
"""\Wdevice_name="({host}[\w\-.]+)"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wlog_subtype="({action}[^"]+)""""
"""\Wuser_name="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""\Wuser_name="({email_address}[^\s@"]+@[^\s@"]+)""""
"""\W(http_)?category="(None|({category}[^"]+))""""
"""\Wurl="(|({url}(({protocol}[^:\\\/\s"]+):[\\\/]+)?({web_domain}[^\\\/\s:"]+)(:\d+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))""""
"""\Wsrc(_ip)?="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"*"""
"""\Wdst(_ip)?="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"*"""
"""\W(spt|src_port)=({src_port}\d+)"""
"""\W(dpt|dst_port)=({dest_port}\d+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wprotocol="({protocol}[^"]+)""""
"""\W(in|recv_bytes|bytes_received)=({bytes_in}\d+)"""
"""\W(out|sent_bytes|bytes_sent)=({bytes_out}\d+)"""
"""\W(http_)?user_agent\\?="({user_agent}[^"]+)""""
"""\W(status_code|http_status)\\?="({http_response_code}\d+)"""
"""\W(dntdom|domain)="?({web_domain}[^\s]+?)""""
"""\W(fname|file_name)="?(|({file_name}[^"]+?))"?\s+(\w+=|$)"""
"""\Wcontenttype="({mime}[^"]+)"""
"""\Wsrc_zone="({src_network_zone}[^"]+)""""
"""\Wdst_zone="({dest_network_zone}[^"]+)""""
"""\Wsrc_country="({src_country}[^"]+)""""
"""\Wdst_country="({dest_country}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```