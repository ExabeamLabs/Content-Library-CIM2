#### Parser Content
```Java
{
Name = sophos-utm-kv-http-session-success-access
   ParserVersion = v1.0.0
   Vendor = Sophos
   Product = Sophos UTM
   TimeFormat = "yyyy:MM:dd-HH:mm:ss"
   Conditions = [
""" name="http access""",
""" fullreqtime="""
   ]
   Fields = [
     """({time}\d\d\d\d:\d\d:\d\d-\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)""",
     """sub="(|({protocol}[^"]+))"""",
     """\saction="(|({action}[^"]+))"""",
     """method="(|({method}[^"]+))"""",
     """srcip="(|({src_ip}[^"]+))"""",
     """dstip="(|({dest_ip}[^"]+))"""",
     """user="(|({user}[^"]+))"""",
     """statuscode="(|({http_response_code}\d+))"""",
     """url="({url}[^"]+)"""",
     """url="(?:-|({protocol}[^:]+))""",
     """url="(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s"]+)""",
     """url="(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))""",
     """url="(?:[^:]+:\/+)({web_domain}[^\/:\s]+)""",
     """referer="(|({referrer}[^"]+))"""",
     """ua="(|({user_agent}[^"]+))""",
     """category="({category}[^"]+)"""",
     """content-type="({mime}[^"]+)"""",
   ]
 

}
```