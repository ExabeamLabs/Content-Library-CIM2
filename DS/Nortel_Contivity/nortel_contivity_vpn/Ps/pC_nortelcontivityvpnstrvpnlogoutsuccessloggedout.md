#### Parser Content
```Java
{
Name = nortelcontivity-vpn-str-vpn-logout-success-loggedout
  Vendor = Nortel Contivity
  Product = Nortel Contivity VPN
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """Security""", """logged out""", """tEvtLgMgr""" ]
  Fields = [ """\w+\s+\d+ \d+:\d+:\d+ ({host}[\w.\-]+)""",
             """({time}\d+/\d+/\d+ \d+:\d+:\d+)""",
             """\[({user}[\w\.\-]{1,40}\$?)\]:({contivity_session_id}\d+) logged out""" 
  ]
  ParserVersion = "v1.0.0"


}
```