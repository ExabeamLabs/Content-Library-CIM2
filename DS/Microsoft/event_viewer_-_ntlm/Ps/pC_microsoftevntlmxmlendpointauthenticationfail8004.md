#### Parser Content
```Java
{
Name = "microsoft-evntlm-xml-endpoint-authentication-fail-8004"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - NTLM"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Conditions = [
        """<Provider Name =""", """Microsoft-Windows-Security-Netlogon""","""<EventID>8004<""", """<Channel>Microsoft-Windows-NTLM/Operational</Channel>"""
    ]
    Fields = [
        """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)('|")/>""",
        """<EventRecordID>({event_id}\d+)<""",
        """<Data Name =('|")UserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
        """<EventID>({event_code}\d+)<""",
        """<Computer>({host}[\w\-\.]+)<""",
        """<Security UserID=('|")({user_sid}S-\d(?:-[\d]+)+)('|")/>""",
        """<Data Name =('|")SChannelName('|")>({dest_host}[\w\.-]+)<""",
        """<Data Name =('|")DomainName('|")>({domain}[\w\.-]+)<""",
        """<Data Name =('|")WorkstationName('|")>({src_host}[\w\.-]+)<"""
        """<Channel>({channel}[^<]+)<"""
    ]


}
```