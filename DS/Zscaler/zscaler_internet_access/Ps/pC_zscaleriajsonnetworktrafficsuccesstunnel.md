#### Parser Content
```Java
{
Name = zscaler-ia-json-network-traffic-success-tunnel
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  ExtractionType = json
  Conditions = [ """"tunneltype":"""", """"sourceip":"""", """IKE""", """Tunnel""" ]
  Fields = [
    """exa_json_path=$..datetime,exa_field_name=time""",
	"""exa_json_path=$..Recordtype,exa_field_name=event_name""",
	"""exa_json_path=$..sourceip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
	"""exa_json_path=$..destinationip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
	"""exa_json_path=$..tunneltype,exa_field_name=vpn_client_type""",
	"""exa_json_path=$..location,exa_field_name=location""", 
	"""exa_json_path=$.event.event,exa_field_name=additional_info""",
	"""exa_json_path=$..eventreason,exa_field_name=result_reason,exa_match_expr=!InList(toLower($..eventreason), "none")""",
	"""exa_json_path=$..user,exa_regex=((\d{1,3}\.){3}\d{1,3}|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  ]


}
```