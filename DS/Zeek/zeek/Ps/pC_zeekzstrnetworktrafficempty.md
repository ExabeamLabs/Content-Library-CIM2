#### Parser Content
```Java
{
Name = zeek-z-str-network-traffic-empty
    Vendor = Zeek
    Product = Zeek 
    TimeFormat = "epoch_sec"
    Conditions = [ "\tT\tF\t", "\t(empty)" ]
    Fields = [
      """^[^\t]*?({time}\d{10})\.\d{3,}\t({host}[^\s\t]+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t)({src_ip}[a-fA-F\d.:]+|[\w.\-]+)\t({src_port}\d+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t){3}({dest_ip}[a-fA-F\d.:]+|[\w.\-]+)\t({dest_port}\d+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t){5}({protocol}[^\t]+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t){6}({service_name}[^\t]+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t){8}({bytes_in}\d+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t){9}({bytes_out}\d+)""",
      """^[^\t]*\d+\.\d+\t([^\t]+\t){10}({connection_state}[^\t]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```