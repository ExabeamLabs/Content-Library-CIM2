#### Parser Content
```Java
{
Name = "watchguard-w-leef-http-request-httprequest"
ParserVersion = "v1.0.0"
Conditions = [
"""LEEF:""",
"""|WatchGuard|XTM|""",
"""msg=HTTPS Request""",
"""policy="""
]

watchguard-events = {
  Vendor = "Watchguard"
  Product = "Watchguard"
  TimeFormat = "MMM dd yyyy HH:mm:ss z"
  Fields = [
		"""\sdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d [\+\-]\d+)"""
		"""serial=({serial_num}[^\s]+)"""
		"""sys_name=({host}[\w\-.]+)"""
		"""\spolicy=({policy_name}[^\s]+)"""
		"""\sdisp=({action}[^\s]+)"""
		"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
		"""\ssrcPort=({src_port}\d+)"""
		"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
		"""\sdstPort=({dest_port}\d+)"""
		"""proto=({protocol}[^\s]+)\s"""
		"""proxy_act=({proxy_action}[^\s]+)"""
		"""rule_name=({rule}[^\s]+)"""
		"""\smsg=({event_description}[^:,]+)"""
		"""\stcp_flag=({tcp_flags}[^\s]+)"""
		"""\ssent_bytes=({bytes_out}\d+)"""
		"""\srcvd_bytes=({bytes_in}\d+)"""
    ] 
   }
  }
DLWatchguard-parser-template = {
  watchguard-events = {
  Vendor = "Watchguard"
  Product = "Watchguard"
  TimeFormat = "MMM dd yyyy HH:mm:ss z"
  Fields = [
		"""\sdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d [\+\-]\d+)"""
		"""serial=({serial_num}[^\s]+)"""
		"""sys_name=({host}[\w\-.]+)"""
		"""\spolicy=({policy_name}[^\s]+)"""
		"""\sdisp=({action}[^\s]+)"""
		"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
		"""\ssrcPort=({src_port}\d+)"""
		"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
		"""\sdstPort=({dest_port}\d+)"""
		"""proto=({protocol}[^\s]+)\s"""
		"""proxy_act=({proxy_action}[^\s]+)"""
		"""rule_name=({rule}[^\s]+)"""
		"""\smsg=({event_description}[^:,]+)"""
		"""\stcp_flag=({tcp_flags}[^\s]+)"""
		"""\ssent_bytes=({bytes_out}\d+)"""
		"""\srcvd_bytes=({bytes_in}\d+)"""
    ] 
   }
  }
#============================================== Start of DefaultParsersAA section ==================================================================
DefaultParsersAA = [

{
Name = "appsense-am-leef-alert-trigger-success-warning"
Vendor = "AppSense"
Product = "AppSense Application Manager"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""AppSense Application Manager"""
"""SourceName ="""
"""Message="""
"""EventCode="""
]
Fields = [
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""ComputerName =({dest_host}[^\s]+)"""
"""Sid=({dest_user_sid}[^\s]+)"""
"""\s+Type=({alert_severity}[^\s]+)"""
"""\'\w+:\\+(?i)users\\+({user}[\w\.\-]{1,40}\$?)"""
"""Hash:({hash_md5}[^\s\]]+)"""
"""Vendor:\s+({process_vendor}[^\]]+)"""
"""Message=AppSense Application Manager ({alert_name}.+?)\s+(of [^\w]|\'|for)"""
"""Message=(The file )?\'.+?\'( has had)?\s+({alert_name}.+?)\s*(\.|of|for)"""
"""Message=\'(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\'"""
"""\'({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?))(\s+\[\w+:|')"""
]
DupFields = [
"process_path->path"
"dest_host->host"
"alert_name->alert_type"
"user_sid->account_id"
]
ParserVersion = "v1.0.0"
}


{
  Name = openvpn-ov-json-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
""" openvpn[""" 
"""MULTI_sva: pool returned """
"""IPv4=""" 
]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """ openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """hostname":"({host}[^"]+)"""
  ]
  DupFields = [ "user->account" 
}
```