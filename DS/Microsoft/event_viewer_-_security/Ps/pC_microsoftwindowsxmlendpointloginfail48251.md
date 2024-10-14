#### Parser Content
```Java
{
Name = microsoft-windows-xml-endpoint-login-fail-4825-1
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""<EventID>4825</EventID>""", """Microsoft-Windows-Security-Auditing""" ]
    Fields = [
      """TimeCreated SystemTime(\\)?=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """<EventID>({event_code}\d+)</EventID>""",
      """<Data Name(\\)?=('|")AccountName('|")>(?=\w)?(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>""",
      """<Data Name(\\)?=('|")AccountDomain('|")>(-|({domain}[^<]+))<\/Data>""",
      """<Data Name(\\)?=('|")LogonID('|")>({login_id}\w+)<\/Data>""",
      """<Data Name(\\)?=('|")ClientAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))<\/Data>""",
      """<Message>({event_name}A user was denied the access to Remote Desktop).""",
      """<Level>({run_level}[^<]+)<"""
    ]
    ParserVersion = "v1.0.0"
  

}
```