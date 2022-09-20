#### Parser Content
```Java
{
Name = dell-sonicwallaventail-kv-vpn-logout-success-infosystem
  Vendor = Dell
  Product = SonicWALL Aventail
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss"
  Conditions = [ """Info System Session End:""",]
  Fields = [
    """:\s.+?\]\s+({host}[^\s]+).+?\sEnd:.+?\(({user}[^\)]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```