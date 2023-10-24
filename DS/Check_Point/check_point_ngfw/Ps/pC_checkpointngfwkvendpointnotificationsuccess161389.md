#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-endpoint-notification-success-161389
ParserVersion = v1.0.0
Conditions = [ """CheckPoint 161389""", """flags:""", """loguid:""" ]

cef-checkpoint-firewall-1 = {
Vendor = Check Point
Product = Check Point NGFW
TimeFormat = "epoch_sec"
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
"""time:"({time}\d{10})""""
"""\W({host}[\w\-.]+) CheckPoint"""
"""\Wifdir:"({direction}[^"]+)"""
"""loguid:"({log_uid}[^"]+)"""
"""origin:"({origin_ip}[^"]+)"""
"""product:"({product_name}[^"]+)"""
"""\Wdescription:"({additional_info}[^"]+)"""
"""version+:"({version}\d+)""""
"""status:(null|"({status}[^"\s]+))"""
"""client_ip:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""

}
```