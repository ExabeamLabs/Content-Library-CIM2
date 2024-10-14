#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-password-read-success-5382
   Product = Event Viewer - Security
   Vendor = Microsoft
   ParserVersion = v1.0.0
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
   Conditions = [ """<EventID>5382<""", """Microsoft-Windows-Security-Auditing""" ]
   Fields =[
      """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
      """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """<EventID>({event_code}\d+)</EventID>""",
      """<Data Name(\\)?=('|")AccountName('|")>(?=\w)?(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>""",
      """<Data Name(\\)?=('|")AccountDomain('|")>(-|({domain}[^<]+))<\/Data>""",
      """<Data Name(\\)?=('|")LogonID('|")>({login_id}\w+)<\/Data>""",
      """<Data Name(\\)?=('|")ClientAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))<\/Data>""",
      """<Level>({run_level}[^<]+)<"""
     ]
   

}
```