#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-ds-object-activity-success-4662-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """|43-263046620|""", """|An operation was performed on an object|""" ]
  Fields = [
    """({event_name}An operation was performed on an object)""",
    """\Wrt=({time}\d{13})""",
    """({host}\S+)\s+CEF:\d+\|"""
    """\|43-2630({event_code}4662)0\|""",
    """\Wact=({result}.+?)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsntdom=({domain}.+?)\s+(\w+=|$)""",
    """\Wshost=({src_host}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\WnitroSecurity_ID=({user_sid}.+?)\s+(\w+=|$)""",
    """\WnitroSource_Logon_ID=({login_id}.+?)\s+(\w+=|$)""",
    """\WnitroLogon_Type=({login_type}\d+)\s+(\w+=|)"""
  ]
  ParserVersion = "v1.0.0"


}
```