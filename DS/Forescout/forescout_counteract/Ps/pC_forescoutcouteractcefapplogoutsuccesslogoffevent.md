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
    """rt=({time}\d{13})""",
    """dvchost=({host}[^\s]+)\s\w+=""",
    """dvc=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """dhost=({dest_host}[^\s]+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """duser=(administrator|User|defaultuser1|({user}[^\s<]+))(<space>\(local\))?\s\w+=""",
    """dntdom=({domain}[^=]+?)\s\w+=""",
    """dmac=({dest_mac}[^\s]+)\s\w+=""",
    """cs2=({event_name}[^=]+?)\s\w+="""
  ]


}
```