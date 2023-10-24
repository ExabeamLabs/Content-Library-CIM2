#### Parser Content
```Java
{
Name = "cisco-asa-mix-app-notification-eigrp"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """EIGRP""", """%DUAL""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s(pdt|PDT):""",
    """dvc=({host}[^\s]+)""",
    """({protocol}EIGRP)""",
    """ad.mnemonic=({event_code}.*?)\sad.message""",
    """ad.message=({event_name}.*?)\said=""",
    """ad.message=({event_name}.+):\s({additional_info}.+)\said""",
# neighbor_ip is removed
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec"]
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```