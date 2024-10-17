#### Parser Content
```Java
{
Name = "symantec-fireglass-cef-http-session-isolation"
Vendor = "Symantec"
Product = "Symantec Fireglass"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Conditions = [
"""|Symantec|Threat Isolation|"""
"""CEF:"""
"""sntdom="""
"""cs4Label=URL Categories"""
"""sourceServiceName ="""
]
Fields = [
"""\|rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""spt=({src_port}\d+)"""
"""dpt=({dest_port}\d+)"""
"""dvchost=({host}[^\s]+)"""
"""act=({action}[^=]+?)\s\w+="""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+="""
"""request=({url}(({protocol}[^:]+):\/\/)?({web_domain}[^\/:\s]+)({uri_path}\/[^\?\s]*)?(({uri_query}\?[^\s]+))?)\s\w+="""
"""requestMethod=({method}[^=]+?)\s\w+="""
"""dhost=({dest_host}[^\s]+)\s\w+="""
"""sntdom=({domain}[^\s]+)"""
"""in=({bytes_out}\d+)"""
"""out=({bytes_in}\d+)"""
"""outcome=({action}[^\s]+)\s\w+="""
"""cs4=({category}[^\s]+)\scs4Label=URL Categories"""
"""requestClientApplication=({user_agent}[^=]+)\s\w+="""
"""requestContext=({referrer}[^\s]+)\s\w+="""
"""cn2=({http_response_code}\d+) cn2Label=Response Status Code"""
]
ParserVersion = "v1.0.0"


}
```