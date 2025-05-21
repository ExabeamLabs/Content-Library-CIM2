#### Parser Content
```Java
{
Name = claroty-ctd-cef-alert-trigger-success-knownthreatalert
    Vendor = Claroty
    Product = CTD
    ParserVersion = v1.0.0
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = ["""CEF:0|Schneider""","""|CTD|""", """Known Threat Alert""", """CtdSignaturePoweredBy=Claroty"""]
    Fields = [
       """CtdSourceIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
       """CtdDestinationIp=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
       """CtdSourceMac=({src_mac}[^\s]+)"""
       """CtdDestinationMac=({dest_mac}[^\s]+)"""
       """CtdSourceHost=({src_host}[\w.-]+)"""
       """CtdDestinationHost=({dest_host}[\w.-]+)"""
       """CtdTimeGenerated=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
       """CtdDeviceExternalId=({device_id}[^=]+)\s+\w+="""
       """CtdMessage=({alert_name}[^=]+)\s+\w+="""
       """CtdAlertLink=({additional_info}[^\s]+)"""
       """CtdAlertScore=({alert_severity}\d+)"""
       """CtdSignatureCriticality=({alert_severity}[^=]+)\s+\w+="""
       """({alert_type}Known Threat Alert)"""
    ]


}
```