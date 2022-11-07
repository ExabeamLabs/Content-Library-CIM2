#### Parser Content
```Java
{
Name = microsoft-windows-kv-network-traffic-success-networkconn-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """AddressFamily=""", """PacketType=""", """RemoteHostName =""", """UserSid=""" ]
  Fields = [
    """TransportHeaderSizeBytes=({bytes}\d+)""",
    """PacketType=({operation}.+?)\s*PacketTypeId=""",
    """RemoteAddress=({dest_ip}[^\s]+)\s+""",
    """RemotePort=({dest_port}\d+)\s*ProcessName =""",
    """Direction=({direction}.+?)\s*Protocol=""",
    """RemoteHostName =({host}[^\s]+)\s+""",
    """ProcessName ="*(unknown|(({process_name}({process_dir}([^\\]+\\)+)?({process_path}.+?))))"*\s*UserName =""",
    """Protocol=({protocol}.+?)\s*ProtocolId=""",
    """LocalAddress=({src_ip}[^\s]+)\s+""",
    """LocalPort=({src_port}\d+)\s*RemoteHostName =""",
    """UserSid=(unknown|({user_sid}.+?))\s*UserId=""",
    """UserName ="*(unknown|((nt authority|({domain}[^\\\/]+))[\\\/])?([Ss]ystem|localsystem|network service|({user}.+?)))"*\s*UserSid=""",
    """UserId=({user_id}.+?)\s*HeaderSizeBytes=""",
  ]


}
```