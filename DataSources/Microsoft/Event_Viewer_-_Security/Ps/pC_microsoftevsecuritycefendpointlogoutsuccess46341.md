#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-logout-success-4634-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """|43-263046340|""", """|An account was logged off.|""" ]
  Fields = [
    """({event_name}An account was logged off)""",
    """\Wrt=({time}\d+)""",
    """({host}\S+)\s+CEF:\d+\|"""
    """\|43-2630({event_code}4634)0\|""",
    """\Wact=({action}.+?)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wsntdom=({domain}.+?)\s+(\w+=|$)""",
    """\Wshost=({src_host}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}.+?)\s+(\w+=|$)""",
    """\WnitroSecurity_ID=({user_sid}.+?)\s+(\w+=|$)""",
    """\WnitroSource_Logon_ID=({login_id}.+?)\s+(\w+=|$)""",
    """\WnitroLogon_Type=({login_type}\d+)\s+(\w+=|)"""
  ]


}
```