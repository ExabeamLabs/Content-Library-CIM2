#### Parser Content
```Java
{
Name = "cisco-fp-kv-alert-trigger-success-intrusioneventrecordipv4"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "dd MMM yyyy HH:mm:ss"
Conditions = [
"""DeviceType=Estreamer"""
"""recordType=INTRUSION_EVENT_RECORD_IPV4"""
]
Fields = [
"""\Wtimestamp=({time}\d\d \w{3} \d{4} \d\d:\d\d:\d\d)"""
"""\WDeviceAddress=({host}[\w\-.]+)"""
"""\WeventId=({alert_id}\d+)"""
"""\WsourceAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WdestinationAddress=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\WsourcePortOrICMPType=({src_port}\d+)"""
"""\WdestinationPortOrICMPCode=({dest_port}\d+)"""
"""\WuserId=({user}[^\s]+)"""
"""\Wrule.message=({alert_name}.+?)\s+([\w\.]+=|$)"""
"""\WpriorityRef=({alert_severity}.+?)\s+([\w\.]+=|$)"""
"""\WrecordType=({alert_type}.+?)\s+([\w\.]+=|$)"""
]
ParserVersion = "v1.0.0"


}
```