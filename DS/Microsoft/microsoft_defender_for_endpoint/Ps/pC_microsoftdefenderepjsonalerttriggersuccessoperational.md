#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-operational
  ExtractionType = json
  ParserVersion = v1.0.0  
  Vendor = Microsoft  
  Product = Microsoft Defender for Endpoint  
  TimeFormat = "yyyy-MM-dd HH:mm:ss"  
  Conditions = ["""Microsoft-Windows-Windows Defender/Operational""" , """Severity ID"""] 
  Fields =[ 
     """exa_json_path=$.Hostname,exa_field_name=host"""
     """exa_json_path=$.EventTime,exa_field_name=time"""
     """exa_json_path=$.['Category Name'],exa_field_name=alert_name"""
     """exa_json_path=$.SeverityValue,exa_field_name=alert_severity"""
     """exa_json_path=$.['Category ID'],exa_field_name=alert_type"""
     """exa_json_path=$.['Threat Name'],exa_field_name=category"""
     """exa_json_path=$.Domain,exa_field_name=domain"""
     """exa_json_path=$.AccountName,exa_field_name=account"""
     """exa_json_path=$.['Detection User'],exa_regex=([^\\]+)\\*({user}[\w\.\-]{1,40}\$?)"""
     """exa_regex="Detection ID":\s*"\{({alert_id}[^\}]+)\}"""
     """exa_json_path=$.Path,exa_field_name=file_path"""
     """exa_json_path=$.Path,exa_regex=(?:({file_dir}[^"]+?)\\+[^"\\;]+)"""
     """exa_json_path=$.Path,exa_regex=[^"]+\\({file_name}[^";,\s\&]+(\.({file_ext}[^"\\.;\s\&\-]+)))"""
     """exa_json_path=$.['UserID'],exa_field_name=user_sid"""
     """exa_json_path=$.['Action Name'],exa_field_name=result"""
     """exa_json_path=$.['Additional Actions String'],exa_field_name=additional_info"""
     """exa_json_path=$.['Error Description'],exa_field_name=failure_reason"""
     """exa_regex="Process Name":\s*"(?:Unknown|({process_path}({process_dir}[^"]+?)(\\+({process_name}[^"\\]+))?))""""
  ] 
},  
{ 
    Name = microsoft-evsystem-kv-dcom-activate-fail-10016  
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - System 
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = ["""Event ID: 10016""","""The application-specific permission settings do not grant""","""for the COM Server application"""] 
    Fields = [  
      """ComputerName(:|=)\s*({host}[\w.-]+)""",  
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """Event ID:\s*({event_code}\d+)""",  
      """({failure_reason}The application-specific permission settings do not grant ({operation}.*) permission for the COM Server application)""",  
      """CLSID\s+\{({cls_id}[^\}]+)\}\s+""", 
      """APPID\s+\{({app_id}[^\}]+)\}\s+""", 
      """user\s+({domain}[^\\]+)\\({user}[\w\.\-]{1,40}\$?)\s""", 
      """\s+SID\s+\(({user_sid}[^\)]+)\)\s+from address\s+(({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[^\s]+))\s""" 
    ] 
    DupFields = ["host->dest_host"] 
  },  

{ 
    Name = microsoft-evadfs-kv-endpoint-login-success-1149 
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - ADFS 
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = [ """Event ID: 1149""", """Remote Desktop Services: User authentication succeeded:"""  ] 
    Fields = [  
      """Event ID:\s*({event_code}\d+)""",  
      """ComputerName(:|=)\s*({host}[\w.-]+)""" 
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """User authentication succeeded:\s*User:\s*({user}[\w\.\-]{1,40}\$?)\s+""", 
      """Domain:\s*({domain}[^\s]+)\s+""", 
      """Source Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""  
    ] 
    DupFields = [ "host->dest_host" ] 
  },  

  { 
    Name = microsoft-evadfs-kv-endpoint-logout-success-148 
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - ADFS 
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = [ """Event ID: 148""", """has been closed between the server"""  ] 
    Fields = [  
      """Event ID:\s*({event_code}\d+)""",  
      """ComputerName(:|=)\s*({host}[\w.-]+)""" 
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """({app}Rdp)CoreTS""", 
      """({operation}Channel ({channel}[^\s]+) has been closed between the server and the client)"""  
    ] 
    DupFields = [ "host->dest_host" ] 
  },  

  { 
    Name = microsoft-windows-kv-file-write-success-216  
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - Application
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = [ """Event ID: 216""","""A database location change was detected""" ]  
    Fields = [  
      """ComputerName(:|=)\s*({host}[\w.-]+)\s+({process_name}[^\s]+)\s+""",  
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """Event ID:\s*({event_code}\d+)""",  
      """\(({process_id}\d+).*\)""",  
      """({operation}A database location change) was detected from\s+\'({src_file_path}({src_file_dir}(?:[^";]+)?[\\\/;])?({src_file_name}[^\\\/";]+?(\.({src_file_ext}[^\\\/\.;"]+))))'\s+to\s+\'({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))))\'\.""" 
    ] 
    DupFields = [ "host->dest_host" ] 
  },  

  { 
    Name = microsoft-windows-kv-file-write-success-325  
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - Application
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = [ """Event ID: 325""","""The database engine created a new database""" ] 
    Fields = [  
      """ComputerName(:|=)\s*({host}[\w.-]+)\s+({process_name}[^\s]+)\s+""",  
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """Event ID:\s*({event_code}\d+)""",  
      """\(({process_id}\d+).*\)""",  
      """({operation}The database engine created a new database)\s+\(\d+,\s+({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))))\)\.""" 
    ] 
    DupFields = [ "host->dest_host" ] 
  },  

  { 
    Name = microsoft-windows-kv-file-read-success-326 
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - Application
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = [ """Event ID: 326""","""The database engine attached a database""" ]  
    Fields = [  
      """ComputerName(:|=)\s*({host}[\w.-]+)\s+({process_name}[^\s]+)\s+""",  
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """Event ID:\s*({event_code}\d+)""",  
      """\(({process_id}\d+).*\)""",  
      """({operation}The database engine attached a database)\s+\(\d+,\s+({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))))\)\."""  
    ] 
    DupFields = [ "host->dest_host" ] 
  },  

  { 
    Name = microsoft-windows-kv-file-close-success-327 
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - Application
    TimeFormat = "yyyy-MM-dd HH:mm:ss"  
    Conditions = [ """Event ID: 327""","""The database engine detached a database""" ]  
    Fields = [  
      """ComputerName(:|=)\s*({host}[\w.-]+)\s+({process_name}[^\s]+)\s+""",  
      """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""", 
      """Event ID:\s*({event_code}\d+)""",  
      """\(({process_id}\d+).*\)""",  
      """({operation}The database engine detached a database)\s+\(\d+,\s+({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))))\)\."""  
    ] 
    DupFields = [ "host->dest_host" ] 
  },  

{
  Name = microsoft-evadfs-xml-ds-object-create-success-4928
  Vendor = Microsoft
  Product = Event Viewer - ADFS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """<EventID>4928</EventID>""", """<Execution ProcessID""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """({event_code}4928)""",
    """<Data Name\\*=('|")DestinationDRA('|")>({ds_object_dn}CN=.*?DC=.*?)</Data>""",
    """<Data Name\\*=('|")SourceDRA('|")>({src_ds_object_dn}CN=.*?DC=.*?)</Data>""",
    """<Data Name\\*=('|")SourceAddr('|")>({src_host}[\w\-.]+)</Data>""",
    """<Data Name\\*=('|")NamingContext('|")>({naming_context}[^\s]+)</Data>""",
    """<Data Name\\*=('|")Options('|")>({options}\d+)</Data>""",
    """<Data Name\\*=('|")StatusCode('|")>({status_code}\d+)</Data>""",
     ]
  

}
```