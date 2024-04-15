#### Parser Content
```Java
{
Name = "cisco-adc-str-http-session-success-adcapp"
Vendor = "Cisco"
Product = "Cisco ADC"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss"
Conditions = [
"""] """
""" ["""
"""[ADC_APP]"""
]
Fields = [
"""\[({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\]\[\d+\]\[\S+\]\[\]\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d)\s+\+\d+\]\s({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s[\S]*\s+({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})?\s({dest_translated_port}\d+)?\s"({uri_path}\S+)"\s"({method}\S+)?\s\S*\s({protocol}\S+)?"\s"({url}\S+)?"\s"({user_agent}.+?)\s*($|\w+=|"|')"""
]
ParserVersion = "v1.0.0"


}
```