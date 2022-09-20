#### Parser Content
```Java
{
Name = forescout-couteract-cef-app-logout-success-logoffevent
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat="epoch"
  Conditions = [ """CEF:""", """|ForeScout Technologies|CounterAct""", """|COMPLIANCE|host is compliant|""", """Interactive Logon Events""", """Logoff Event """ ]
  Fields = [
    """rt=({time}\d+)""",
    """dvchost=({host}[^\s]+)\s\w+=""",
    """dvc=({host_ip}[a-fA-F\d:\.]+)""",
    """dhost=({dest_host}[^\s]+)""",
    """dst=({dest_ip}[a-fA-F\d:\.]+)""",
    """duser=(administrator|User|defaultuser1|({user}[^\s<]+))(<space>\(local\))?\s\w+=""",
    """dntdom=({domain}[^=]+?)\s\w+=""",
    """dmac=({dest_mac}[^\s]+)\s\w+=""",
    """cs2=({event_name}[^=]+?)\s\w+="""
  ]


}
```