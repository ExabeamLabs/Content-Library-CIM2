#### Parser Content
```Java
{
Name = microsoft-windows-xml-endpoint-login-fail-4825
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""<EventID>4825</EventID>""", """<Provider>Microsoft Windows security auditing.</Provider>""", """<Message>A user was denied the access to Remote Desktop."""]
    Fields = [
      """TimeCreated SystemTime(\\)?=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """<EventID>({event_code}\d+)</EventID>""",
      """<Data Name(\\)?='AccountName'>(?=\w)?(-|({user}[\w\.\-]{1,40}\$?))<\/Data>""",
      """<Data Name(\\)?='AccountDomain'>(-|({domain}[^<]+))<\/Data>""",
      """<Data Name(\\)?='LogonID'>({login_id}\w+)<\/Data>""",
      """<Data Name(\\)?='ClientAddress'>({src_ip}[a-fA-F0-9\.:]+)<\/Data>""",
      """<Message>({event_name}A user was denied the access to Remote Desktop).""",
      """<Level>({run_level}[^<]+)<"""
    ]
    ParserVersion = "v1.0.0"
  

}
```