#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-network-session-success-3
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
"""<Provider Name"""
"""'Microsoft-Windows-Sysmon'""",
"""<EventID>3</EventID>"""
  ]
  Fields = [
    """<Provider Name\\*='Microsoft-Windows-Sysmon' Guid='\{({process_guid}[^}]+?)\}"""
    """<EventID>({event_code}\d+)<\/EventID>"""
    """<Task>({operation}.*?)<\/Task>"""
    """<Execution ProcessID\\*='({process_id}\d+)"""
    """UtcTime:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """<Computer>({host}.+?)<\/Computer>"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
    """<Security UserID\\*='(({domain}[^\\]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s*\/>"""
    """<EventData>.*?Image:\s*({process_path}({process_dir}.*?)({process_name}[^.]+\.exe))\s*User:"""
    """<EventData>.*?Image:\s*({path}.+?)\s*User:"""
    """SourceIp:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """SourceHostname:\s*({src_host}.*?)\s*(Source|$)"""
    """<EventData>.*?<Data Name\\*='UtcTime'>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """<EventData>.*?<Data Name\\*='ProcessGuid'>\{({process_guid}[^}]+)\}<\/Data>"""
    """<EventData>.*?<Data Name\\*='ProcessId'>({process_id}\d+)"""
    """<EventData>.*?<Data Name\\*='Image'>({process_path}({process_dir}(?:[^<>]+)?[\\]+)?({process_name}[^\\<>]+))<\/Data>"""
    """<EventData>.*?<Data Name\\*='User'>(({domain}[^\>]+?\w+))?\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>"""
    """<EventData>.*?<Data Name\\*='Protocol'>({protocol}[^<>]+)<\/Data>"""
    """<EventData>.*?<Data Name\\*='SourceIp'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<EventData>.*?<Data Name\\*='SourceHostname'>(-|({src_host}[^<>]+))</Data>""",
    """<EventData>.*?<Data Name\\*='SourcePort'>({src_port}\d+)""",
    """<EventData>.*?<Data Name\\*='DestinationIp'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<EventData>.*?<Data Name\\*='DestinationHostname'>(-|({dest_host}[\w\-.]+))</Data>""",
    """<EventData>.*?<Data Name\\*='DestinationPort'>({dest_port}\d+)""",
    """<Level>({run_level}[^<]+)<"""
 ]


}
```