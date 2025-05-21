#### Parser Content
```Java
{
Name = cylance-optics-kv-alert-trigger-success-powershellevent
  ParserVersion = v1.0.0
  Conditions = [ """CylanceOPTICS""", """Event Type: OpticsCaePowershellTraceEvent""" ]

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
    """Process Name:\s*(|({process_name}[^,]+)),"""
    """Process Owner:\s*(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\/\/+)?(?:SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """Device Id:\s*({device_id}[^",]+)"""
    """Target Domain Name:\s*({dest_domain}[^,]+)"""
    """File Path:\s({file_path}[^,]+)"""
    """Logon Type\s*({login_type}\d+)\s*"""
    """Destination IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """Destination Port:\s*({dest_port}\d+)"""
    """Process Command Line:\s*"+({process_command_line}[^",]+)""""
    """Registry KeyPath:\s*({object}({registry_path}[^,"]*?({registry_key}[^,"\\\/]+?))),"""
    """Registry ValueName:\s*({registry_value}[^,]+)"""
    """Operation:\s*({operation}[^\s]+)"""
    """Instigating Process Owner:\s*({process_owner}[^,]+)"""
    """Target File Path:\s({dest_path}[^,]+)"""
    """Description:\s*({alert_name}[^,]+),"""
  ]
      DupFields = [ "event_category->alert_type" ]


}
```