#### Parser Content
```Java
{
Name = "cisco-fp-kv-dns-request-success-estreamer"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "epoch"
Conditions = [
"""DeviceType=Estreamer"""
"""flowStatistics.dnsQuery="""
]
Fields = [
"""\sDeviceAddress=({host}[\w.\-]+)"""
"""\sCurrentTime=({time}\d{13})"""
"""\sflowStatistics\.initiatorIPAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sflowStatistics\.responderIPAddress=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sflowStatistics\.initiatorPort=({src_port}\d+)"""
"""\sflowStatistics\.responderPort=({dest_port}\d+)"""
"""\sflowStatistics\.dnsQuery=({dns_query}.+?)(\s+flowStatistics\.|\s*$)"""
"""\sflowStatistics\.dnsRecordType=({dns_record_type}\d+)"""
"""\sflowStatistics\.dnsResponseType=({dns_response_type}\d+)"""
"""\sflowStatistics\.dnsTTL=({response_ttl}\d+)"""
"""\sflowStatistics\.bytesSent=({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```