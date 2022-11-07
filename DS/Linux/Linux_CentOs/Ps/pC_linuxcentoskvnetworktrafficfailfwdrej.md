#### Parser Content
```Java
{
Name = linux-centos-kv-network-traffic-fail-fwdrej
  ParserVersion = v1.0.0
  Vendor = Linux
  Product = Linux CentOs
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """KAFKA_CONNECT_SYSLOG""", """[FWD REJ]""", """SRC=""" ]
  Fields =[
    """\d\d\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+kernel:""",
    """SRC=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """DST=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\s+({app}\w+)\s+\[FWD REJ\]""",
    """({action}FWD REJ)""",
    """SPT=({src_port}\d+)""",
    """DPT=({dest_port}\d+)""",
    """PROTO=({protocol}[^\s]+)""",
    """MAC=({src_mac}[^\s]+)""",
    """IN=({src_interface}[^\s]+)""",
    """OUT=({dest_interface}[^\s]+)""",
    """RES=({result}[^\s]+)"""
 ]


}
```