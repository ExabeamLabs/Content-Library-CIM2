#### Parser Content
```Java
{
Name = "forcepoint-wsg-leef-http-session-webactivity"
Vendor = "Forcepoint"
Product = "Websense Security Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Websense|Security|"""
"""|transaction:"""
"""srcBytes="""
]
Fields = [
"""\d{1,2}:\d{1,2}:\d{1,2}\s+({host}[^\s]+)\s*LEEF:"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssrcPort=({src_port}\d+)"""
"""\sdstPort=({dest_port}\d+)"""
"""\susrName =(-|(?!LDAP:)({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
"""\susrName =LDAP:\/\/\S+\s+({user_ou}[^\/]+?)\/({full_name}.+?)\s+\w+="""
"""\|transaction:({action}[^\|]+)"""
"""\smethod=(?:-|({method}[^\s]+))"""
"""\ssrcBytes=({bytes_in}\d+)"""
"""\sdstBytes=({bytes_out}\d+)"""
"""\scontentType=(?:-|({mime}[^=]+)(;.*)?)\s+reason="""
"""\sproxyStatus-code=({http_response_code}\d+)"""
"""\scat=({category_id}\d+)"""
"""\suserAgent=(?:-|({user_agent}.+?))\s+\w+="""
"""\surl=(?:-|({url}[^\s"]+))"""
"""\surl=(?:-|({protocol}[^:]+))"""
"""\surl=(?:[^:]+:\/+)({web_domain}[^\/:\s]+)"""
"""\surl=(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)"""
"""\surl=(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))"""
]
ParserVersion = "v1.0.0"


}
```