#### Parser Content
```Java
{
Name = sophos-utm-kv-http-session-fail-requestblocked
   ParserVersion = v1.0.0
   Vendor = Sophos
   Product = Sophos UTM
   TimeFormat = "yyyy:MM:dd-HH:mm:ss"
   Conditions = [
""" name="web request blocked""",
""" fullreqtime="""
   ]
   Fields = [
     """({time}\d\d\d\d:\d\d:\d\d-\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)""",
     """sub="(|({protocol}[^"]+))"""",
     """action="(|({action}[^"]+))"""",
     """method="(|({method}[^"]+))"""",
     """srcip="(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
     """dstip="(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
     """user="(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
     """statuscode="(|({http_response_code}\d+))"""",
     """url="({url}[^"]+)""",
     """url="(?:-|({protocol}[^:]+))""",
     """url="(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s"]+)""",
     """url="(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))""",
     """url="(?:[^:]+:\/+)({web_domain}[^\/:\s]+)""",
     """referer="(|({referrer}[^"]+))"""",
     """ua="(|({user_agent}[^"]+))"""",
     """category="({category}[^"]+)""",
   ]
 

}
```