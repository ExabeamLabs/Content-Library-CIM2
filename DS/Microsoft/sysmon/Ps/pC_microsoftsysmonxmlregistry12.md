#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-registry-12
  Product = Sysmon
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>12</EventID>""", """<Provider Name""","""<Channel>Microsoft-Windows-Sysmon""" ]
  Fields = ${DLWindowsParsersTemplates.xml-sysmon-activity.Fields}[
    """<Data Name\\*=('|")TargetObject('|")>({registry_path}[^<>]+?[\\\/]+\{?({registry_key}[^\\<]+?)\}?[\\\/]+({registry_value}[^\\<]+))<\/Data>""",
    """<Data Name\\*=('|")EventType('|")>({operation}[^<]+)<""",
    """<Computer>({dest_host}({host}[\w\-.]+?))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

xml-sysmon-activity = {
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """<Provider Name\\*=('|")Microsoft-Windows-Sysmon('|") Guid=('|")\{({process_guid}[^}]+?)\}""",
    """<Data Name\\*=('|")UtcTime('|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """<EventID>({event_code}\d+)</EventID>""",
    """<Task>({operation}.*?)</Task>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Execution.*?ThreadID=('|")({thread_id}\d+)""",
    """<Task>({task_name}[^<]+)<"""
    """<Security UserID\\*=('|")({user_sid}[^']+)('|")//?>""",
    """<Data Name\\*=('|")Image('|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>""",
    """<Data Name\\*=('|")TargetFilename('|")>({file_path}(({file_dir}[^<>]+?)[\\\/]+)?({file_name}[^\\\/<>]*?(\.({file_ext}\w+))?))(:\w+)?<\/Data>""",
    """<Keywords>({result}.+?)<\/Keywords>""",
    """<Data Name\\*=('|")ProcessGuid('|")>\{({process_guid}.+?)\}<\/Data>""",
    """<Data Name\\*=('|")ProcessId('|")>({process_id}\d+)""",
    """<Data Name\\*=('|")State('|")>({state}[^<]+)<""",
    """({log_name}Microsoft-Windows-Sysmon)"""    
    """<Level>({run_level}[^<]+)<"""
   
}
```