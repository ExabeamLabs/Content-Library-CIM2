#### Parser Content
```Java
{
Name = thoughtspot-ts-json-app-activity-success-type
   Vendor = "ThoughtSpot"
   Product = "ThoughtSpot"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
   Conditions =  [ """"date":"""", """\"cIP\":""", """\"type\":""", """"data\":{""", """log":"{""" ]
   Fields = [
     """"ts\\":\\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\\"""",
     """userGUIDs\\"[^=]+?\\"id\\":\\"({user_uid}[^"\\]+)\\""""
     """"userGUID\\":\\"({user_uid}[^"\\]+)\\"""",
     """"userName\\":\\"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\"""",
     """"cIP\\":\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\"""",
     """"type\\":\\"({operation}[^"\\]+)?\\"""",
     """"desc\\":\\"({operation_details}[^"\\]+)?\\"""",
     """"data\\":\{({additional_info}[^\}]+)?\}""",
     """"authType\\":\\"({auth_type}[^"\\]+?)\\"""",
     """"action\\":\\"({event_name}[^"\\]+?)\\"""",
     """"userId\\":\\"({user_id}[^"\\]+?)\\"""",
     """"groupIdentity\\":\{[^\}]+?\\"id\\":\\"({group_id}[^"]+)\\"""",
     """"groupIdentity\\":\{[^=]+?\\"name\\":\\"({group_name}[^"]+)\\"""",
     """"currentDisplayName\\":\\\"({old_value}[^"]+?)\\"""",
     """"modifiedDisplayName\\":\\\"({new_value}[^"]+?)\\"""",
     """"groupNames\\":\\\"({group_name}[^"]+?)\\""""
   ]
   ParserVersion = "v1.0.0"
 

}
```