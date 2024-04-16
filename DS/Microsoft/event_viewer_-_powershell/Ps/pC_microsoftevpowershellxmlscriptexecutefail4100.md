#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-script-execute-fail-4100
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Product = Event Viewer - PowerShell
  Vendor = Microsoft
  Conditions = [ """<EventID>4100</EventID""", """<Provider Name =""", """<Execution ProcessID=""" ]
  Fields =[
    """<Computer>({host}[^<]+)<"""
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)"""
    """<Security UserID='({user_sid}[^'<]+)"""
    """<Data Name ='ContextInfo'>\s*Severity = ({alert_severity}[^\s]+)"""
    """<Data Name ='ContextInfo'>[^@]+?User\s*=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))(\\r|\\n|\\t)*\s*(Connected User|Shell ID) ="""
    """<Data Name ='ContextInfo'>[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version ="""
    """<Data Name ='ContextInfo'>[^@]+?Command Type\s*=\s*(|({command_type}[^=]+?))\s*Script Name"""
    """<Data Name ='ContextInfo'>[^@]+?Command Name\s*=\s*(|({command_name}[^=]+?))\s*Command Type ="""
    """<Data Name ='ContextInfo'>[^@]+?Script Name\s*=\s+({script_name}\S[^=]+?)\s+Command Path ="""
    """Engine Version\s*=\s*({engine_version}[^\s]+)\s"""
    """Data Name ='Payload'>Error Message = ({failure_reason}[^<]+?)\s*<"""
  ]
  

}
```