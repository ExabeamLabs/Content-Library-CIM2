#### Parser Content
```Java
{
Name = hp-arubawc-str-network-notification-success-cli
Vendor = "HP"
Product = "Aruba Wireless controller"
ParserVersion = "v1.0.0"
TimeFormat = ["MMM dd HH:mm:ss yyyy","MMM d HH:mm:ss yyyy"]
Conditions = [ """recv_sta_""", """> AP:""", """ cli[""" ]
Fields = [
  """({time}\w+\s+\d+\s\d\d:\d\d:\d\d(\s\d\d\d\d)?)\s(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))\s+cli\["""
  """({process_name}cli)\[({process_id}\d+)\]:\s<({event_code}\d+)>\s<({severity}[^>]+)>""",
  """>\sAP:\S+\s<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({src_mac}[^>]+)>""",
  """\scli\[\d+\]:\s+<\d+>\s+<\w+>\s({additional_info}.*?)\s*($|cli\[)"""
]


}
```