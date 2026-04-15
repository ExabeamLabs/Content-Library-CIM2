#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-operational
  ExtractionType = json
  ParserVersion = v1.0.0  
  Vendor = Microsoft  
  Product = Microsoft Defender  
  TimeFormat = "yyyy-MM-dd HH:mm:ss"  
  Conditions = [""""Channel":"Microsoft-Windows-Windows Defender/Operational"""" , """"Severity ID":"""] 
  Fields =[ 
     """exa_json_path=$.Hostname,exa_field_name=host"""
     """exa_json_path=$.EventTime,exa_field_name=time"""
     """exa_json_path=$.['Category Name'],exa_field_name=alert_name"""
     """exa_json_path=$.SeverityValue,exa_field_name=alert_severity"""
     """exa_json_path=$.['Category ID'],exa_field_name=alert_type"""
     """exa_json_path=$.['Threat Name'],exa_field_name=category"""
     """exa_json_path=$.Domain,exa_field_name=domain"""
     """exa_json_path=$.AccountName,exa_field_name=account"""
     """exa_json_path=$.['Detection User'],exa_regex=([^\\]+)\\*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
     """exa_regex="Detection ID":\s*"\{({alert_id}[^\}]+)\}"""
     """exa_json_path=$.Path,exa_field_name=file_path"""
     """exa_json_path=$.Path,exa_regex=(?:({file_dir}[^"]+?)\\+[^"\\;]+)"""
     """exa_json_path=$.Path,exa_regex=[^"]+\\({file_name}[^";,\s\&]+(\.({file_ext}[^"\\.;\s\&\-]+)))"""
     """exa_json_path=$.['UserID'],exa_field_name=user_sid"""
     """exa_json_path=$.['Action Name'],exa_field_name=result"""
     """exa_json_path=$.['Additional Actions String'],exa_field_name=additional_info"""
     """exa_json_path=$.['Error Description'],exa_field_name=failure_reason"""
     """exa_regex="Process Name":\s*"(?:Unknown|({process_path}({process_dir}[^"]+?)(\\+({process_name}[^"\\]+))?))""""
     """exa_json_path=$.Channel,exa_field_name=channel"""
  ] 
},  

  { 
    Name = microsoft-evadfs-xml-endpoint-logout-success-148 
    ParserVersion = v1.0.0  
    Vendor = Microsoft  
    Product = Event Viewer - RemoteDesktopServices
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"  
    Conditions = [ """<EventID>148</EventID>""", """Microsoft-Windows-RemoteDesktopServices-RdpCoreTS""" ] 
    Fields = [  
      """<EventID>({event_code}\d+)<""",  
      """<Computer>({dest_host}({host}[\w\-.]+))""",
      """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)""", 
      """({app}Rdp)CoreTS""", 
      """<Data Name =('|")ChannelName('|")>({channel}[^<]+)"""
      """<Level>({run_level}[^<]+)<"""  
    ] 
  

}
```