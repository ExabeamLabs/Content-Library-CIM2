#### Parser Content
```Java
{
Name = linux-centos-kv-network-traffic-fail-fwdrej
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """KAFKA_CONNECT_SYSLOG""", """[FWD REJ]""", """SRC=""" ]
  Fields =[
    """\d\d\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+kernel:""",
    """SRC=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """DST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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