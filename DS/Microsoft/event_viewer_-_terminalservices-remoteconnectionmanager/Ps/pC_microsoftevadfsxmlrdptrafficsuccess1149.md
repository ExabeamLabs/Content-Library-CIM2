#### Parser Content
```Java
{
Name = "microsoft-evadfs-xml-rdp-traffic-success-1149"
    Vendor = Microsoft
    Product = Event Viewer - TerminalServices-RemoteConnectionManager
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    Conditions = [ """<EventID>1149<""", """<Security UserID""", """<Param1>""", """<Computer>""" ]
    Fields = [
      """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """<Computer>({dest_host}({host}[\w\-.]+))<""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """({event_code}1149)""",
      """<Param1>({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^<]+))?<""",
      """<Param2>({domain}[^<]+)<""",
      """<Param3>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
      """<Security UserID\\*='({user_sid}[^']+)'"""
      """<Level>({run_level}[^<]+)<"""
    ]
    ParserVersion = "v1.0.0"


}
```