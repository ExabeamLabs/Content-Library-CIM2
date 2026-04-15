#### Parser Content
```Java
{
Name = sophos-ep-json-app-notification-nocompliant
  ExtractionType = json
  ParserVersion = v1.0.0
  Product = Sophos Endpoint Protection
  Conditions = [ """Event::Endpoint::NonCompliant""" ]

sophos-events-aa = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"location":"({src_host}({host}[^"]+))""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({event_name}[^"]+)""",
    """"type":\s*"({event_category}[^"]+)""",
    """"dhost":\s*"({dest_host}[\w\-.]+)"""",
    """"severity":\s*"({severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"suser":\s*"(n\/a|({full_name}[^"\\\s,]+\s+[^"\\,]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
# id is removed
    """"source":"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\\"source_info\\"__ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source_info":\s*\{"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source":"(({domain}[^\\",]+?)\\+)?(?:n\/a|Administrator|({full_name}(?:({first_name}[^\s",.\\]+)(?:\s+|\.))({last_name}[^",\\]+)))"""",
    """"source":"((({domain}[^\",]+?)\\+)?(?:n/a|Administrator|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """destinationServiceName =({app}[^=]+)\s+\w+="""

    """exa_json_path=$.location,exa_field_name=host""",
    """exa_json_path=$.location,exa_field_name=src_host""",
    """exa_json_path=$.when,exa_field_name=time""",
    """exa_json_path=$.rt,exa_field_name=time""",
    """exa_json_path=$.name,exa_regex=({event_name}[^"':]+)""",
    """exa_json_path=$.type,exa_field_name=event_category""",
    """exa_json_path=$.dhost,exa_field_name=dest_host""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.suser,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
    """exa_json_path=$.source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.source,exa_regex=(?:n\/a|Administrator|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$"""
  sophos-events-aa = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"location":"({src_host}({host}[^"]+))""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({event_name}[^"]+)""",
    """"type":\s*"({event_category}[^"]+)""",
    """"dhost":\s*"({dest_host}[\w\-.]+)"""",
    """"severity":\s*"({severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"suser":\s*"(n\/a|({full_name}[^"\\\s,]+\s+[^"\\,]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
# id is removed
    """"source":"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\\"source_info\\"__ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source_info":\s*\{"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source":"(({domain}[^\\",]+?)\\+)?(?:n\/a|Administrator|({full_name}(?:({first_name}[^\s",.\\]+)(?:\s+|\.))({last_name}[^",\\]+)))"""",
    """"source":"((({domain}[^\",]+?)\\+)?(?:n/a|Administrator|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """destinationServiceName=({app}[^=]+)\s+\w+="""

    """exa_json_path=$.location,exa_field_name=host""",
    """exa_json_path=$.location,exa_field_name=src_host""",
    """exa_json_path=$.when,exa_field_name=time""",
    """exa_json_path=$.rt,exa_field_name=time""",
    """exa_json_path=$.name,exa_regex=({event_name}[^"':]+)""",
    """exa_json_path=$.type,exa_field_name=event_category""",
    """exa_json_path=$.dhost,exa_field_name=dest_host""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.suser,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
    """exa_json_path=$.source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.source,exa_regex=(?:n\/a|Administrator|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$"""
  ]
},

cef-sophos-dlp-alert = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """\Wrt=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^:.\|]+)(:\s({target}[^\|]+))?""",
    """CEF:([^\|]*\|){5}({additional_info}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^:.\|]+).+?Username:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Rule names:\s*′({rule}[^′]+).+?Data Control action:\s*({result}[^\s]+)\s+File type:\s*({file_type}.+?)\s+File size:\s*({bytes}\d+)\s+({additional_info}.+?Destination path:\s*({target}.+?)\s+Destination type:[^\|]*)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
    """\Wdhost=({src_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Wsuser=((({dest_host}[^\s\\]+)\\+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)|(n\/a|({full_name}[^\\]+?)))\s+(\w+=|$)""",
    """\Wid=({alert_id}[^\s]+)""",
  ]
},

cef-sophos-dlp-alert-1 = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"location":"({host}[\w\-.]+)"""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"type":"({alert_type}Event[^"]+)""",
    """"description":"({alert_name}[^"]+?)\.?"""",
    """"name":"({alert_name}[^"]+)""",
    """"group":"({additional_info}[^"]+)""",
    """"name":\s*"(n\/a|({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\'))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"severity":"({alert_severity}[^"]+)""",
    """"id":"({alert_id}[^"]+)""",
    """"location":"({src_host}[^"]+)""",
    """"source":"(n\/a|({full_name}[^"\\\(\),]+))"""",
    """"source":"(n\/a|({last_name}[^",\s]+),\s*({first_name}[^,"\s]+))""",
    """"source":"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+))\\+)?(?:Administrator|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]
},

cef-sophos-security-alert-1 {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"location":"({src_host}({host}((\d{1,3}\.){3}\d{1,3}|({=src_host}[\w\-.]+))))"""",
    """"id":"({alert_id}[^"]+)""",
    """"severity":"({alert_severity}[^"]+)""",
    """"name":\s*"(n\/a|({event_name}({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\')))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({process_path}[^']+\\({process_name}[^']+))))""",
    """"type":"({event_name}({alert_name}Event::Endpoint::[^"]+))""",
    """"name":"({event_name}({alert_name}[^"]+))""",
    """"threat":"?(null|({event_name}({alert_name}[^",]+)))""",
    """"type":"({alert_type}Event::Endpoint::[^"]+)""",
    """"source":"(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\\\(\)]+))","\w+""",
    """"source":"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+?))\\+)?((\d{1,3}\.){3}\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"description":"({additional_info}[^:"]+:?([^"]+? at '({malware_url}[^"]+)')?)"""",
    """"descriptor":"({process_path}[^"]+\\({process_name}[^"]+))"""",
    """"endpoint_platform":"({os}[^"]+)"""
  ]
},
sophos-alert-events = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.when,exa_field_name=time""",
  	"""exa_json_path=$.source,exa_regex=(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\s]+\s[^"]+)$|((({domain}[^\\"]+?))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$)""",
  	"""exa_json_path=$.location,exa_regex=^({host}[\w\-\.]+)$""",
  	"""exa_json_path=$.id,exa_field_name=alert_id""",
  	"""exa_json_path=$.severity,exa_field_name=alert_severity""",
  	"""exa_json_path=$.name,exa_field_name=alert_name""",
  	"""exa_json_path=$.type,exa_field_name=alert_type""",
  	"""exa_json_path=$.description,exa_field_name=additional_info""",
  	"""exa_json_path=$..endpoint_type,exa_field_name=device_type""",
  	"""exa_json_path=$.user_id,exa_field_name=user_id""",
  	"""exa_json_path=$.group,exa_field_name=group_type""",
  	"""exa_json_path=$..source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.location,exa_regex=^({src_host}[\w\-\.]+)$""",
  ]
},

sophos-notification-events = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.when,exa_field_name=time""",
  	"""exa_json_path=$.source,exa_regex=(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\s]+\s[^"]+)$|((({domain}[^\\"]+?))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$)""",
  	"""exa_json_path=$.location,exa_regex=^({host}[\w\-\.]+)$""",
  	"""exa_json_path=$.id,exa_field_name=event_id""",
  	"""exa_json_path=$.severity,exa_field_name=severity""",
  	"""exa_json_path=$.name,exa_field_name=event_name""",
  	"""exa_json_path=$.type,exa_field_name=event_subtype""",
  	"""exa_json_path=$.description,exa_field_name=additional_info""",
  	"""exa_json_path=$..endpoint_type,exa_field_name=device_type""",
  	"""exa_json_path=$.user_id,exa_field_name=user_id""",
    """exa_json_path=$.group,exa_field_name=group_type""",
  	"""exa_json_path=$..source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.location,exa_regex=^({src_host}[\w\-\.]+)$""",
  ]
}
kv-sophos-xgs-event = {
  Vendor = Sophos
  Product = Sophos XGS Firewall
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """timestamp="({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d(\+|\-)\d{4})""",
    """log_id="({event_code}\d+)""",
    """log_type="({event_category}[^"]+)""",
    """log_subtype="({subtype}[^"]+)""",
    """log_component="({app}(Firewall|SSL VPN|CLI|GUI|VPN Portal|AD SSO))""",
    """status="({result}[^"]+)""",
    """severity="({severity}[^"]+)""",
    """user_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s""",
    """auth_mechanism="({auth_method}[^"]+)""",
    """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """message="({additional_info}[^"]+)""",
    """src_country="({src_country}[^"]+)""",
    """bytes_sent="({bytes_out}\d+)""",
    """protocol="({protocol}[^"]+)""",
    """reason="({result_reason}[^"]+)"""
  ]
}
}
}
```