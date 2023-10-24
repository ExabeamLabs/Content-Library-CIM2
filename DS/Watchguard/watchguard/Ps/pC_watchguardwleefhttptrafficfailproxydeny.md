#### Parser Content
```Java
{
Name = "watchguard-w-leef-http-traffic-fail-proxydeny"
ParserVersion = "v1.0.0"
Conditions = [
"""LEEF:""",
"""|WatchGuard|XTM|""",
"""msg=ProxyDeny""",
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
CylanceParserTemplates = {
 
kv-cylance-optics-events = {
  Vendor = Cylance
  Product = Cylance OPTICS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s\S+ CylanceOPTICS""",
    """Event Type:\s*({event_category}[^,]+)""",
    """Event Name: ({event_name}[^,]+)""",
    """Device Name: ({src_host}[^,]+)""",
    """Zone Names: \(({zone}[^\),]+)""",
    """Event Id:\s*({event_code}[^,]+)"""
    """Severity:\s*({alert_severity}[^,]+)"""
    """Description:\s*({additional_info}[^,]+)"""
    """Process Name:\s*({process_name}[^,]+)"""
    """Process Owner:\s*(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\/\/+)?(?:SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
    """Device Id:\s*({device_id}[^",]+)"""
    """Target Domain Name:\s*({dest_domain}[^,]+)"""
    """File Path:\s({file_path}[^,]+)"""
    """Logon Type\s*({login_type}\d+)\s*"""
    """Destination IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """Destination Port:\s*({dest_port}\d+)"""
    """Process Command Line:\s*"+({process_command_line}[^",]+)""""
    """Registry KeyPath:\s*({object}({registry_path}({registry_key}[^,"]+?)\\+\{({registry_value}[^"\\]+)\}))"""
    """Registry ValueName:\s*({registry_value}[^,]+)"""
    """Operation:\s*({operation}[^\s]+)"""
    """Instigating Process Owner:\s*({process_owner}[^,]+)"""
    """Target File Path:\s({dest_path}[^,]+)"""
  ]
      DupFields = [ "event_category->alert_type", "event_name->alert_name" ]


}
```