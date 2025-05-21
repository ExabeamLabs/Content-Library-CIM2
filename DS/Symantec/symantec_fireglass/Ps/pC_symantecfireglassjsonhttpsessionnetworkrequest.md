#### Parser Content
```Java
{
Name = "symantec-fireglass-json-http-session-networkrequest"
Vendor = "Symantec"
Product = "Symantec Fireglass"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""url_categories":"""
""""original_source_ip":"""
""""organization_id":""""
""""isolation_session_id":"""
""""url_host":"""
]
Fields = [
""""time_stamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""\w+\s+\d{1,2}\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
""""top_level_url_scheme":"({protocol}[^"]+)""""
""""source_ip":"({src_translated_ip}[a-fA-F\d:.]+)""""
""""original_source_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""destination_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""source_port":({src_port}\d+)"""
""""url_port":({dest_port}\d+)"""
""""url_host":"({web_domain}[^"]+)""""
""""username":"(({email_address}[^@]+@[^."]+?\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))""""
""""url":"({url}[^"]+)""""
""""response_status_code":({http_response_code}\d+)"""
""""url":"(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s"]+)"""
""""url":"[^"]+?({uri_query}\?[^\s"]+)"""
""""request_method":"({method}[^"]+)""""
""""user_agent":"({user_agent}[^"]+)""""
""""content_type":"({mime}[^"]+)""""
""""referer_url":"({referrer}[^"]+)""""
""""malicious":"({result}[^"]+)""""
""""total_bytes":({bytes}\d+)"""
""""action":"({action}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```