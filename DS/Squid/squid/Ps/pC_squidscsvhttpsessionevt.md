#### Parser Content
```Java
{
Name = "squid-s-csv-http-session-evt"
Vendor = "Squid"
Product = "Squid"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
"""[EVT_"""
""",tk_url="""
""",tk_protocol="""
]
Fields = [
"""\Wtk_date_field=({time}[^,"]+)"""
"""\Wtk_server_ip=({host}[A-Fa-f:\d.]+)"""
"""\Wtk_server=({host}[\w\-.]+)"""
"""\Wtk_username=(({full_name}\w+(\s+\w+)+)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""\Wtk_client_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wtk_url=(-|({url}(({protocol}[^:\\\/\s,]+):[\\\/]+)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?))(:\d+)?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s,]*)?))"""
"""\Wtk_protocol=({protocol}[^,"]+)"""
"""\Wtk_category=(0|({categories}({category}[^,";\/]+)[^,]*))"""
"""\Wtk_file_name=({uri_path}[^,"]+)"""
"""\Wtk_operation=({method}[^,"]+)"""
"""\Wtk_mime_content=(none|({mime}[^,"]+))"""
"""\Wtk_scan_type=({scan_type}[^,"]+)"""
"""\Wtk_rule_name=({rule}[^,"]+)"""
"""\Wtk_filter_action=({action}[^,"\s]+)"""
"""\[({result}EVT_\w+)\s*\|"""
]
ParserVersion = "v1.0.0"


}
```