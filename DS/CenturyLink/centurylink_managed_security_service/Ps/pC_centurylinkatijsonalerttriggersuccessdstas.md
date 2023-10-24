#### Parser Content
```Java
{
Name = "centurylink-ati-json-alert-trigger-success-dstas"
Vendor = "CenturyLink"
Product = "CenturyLink Managed Security Service"
TimeFormat = "epoch_sec"
Conditions = [
"""ati-threatflow"""
""""event_type":"threatflow""""
""""dstAS":"""
]
Fields = [
""""timestamp\":({time}\d{10})"""
""""dstThreat\":"({alert_type}[^\"]+)"""
""""srcThreat\":"({alert_name}[^\"]+)"""
""""agent\":\"({host}[^\"]+)\""""
""""srcAddr\":"({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\""""
""""dstAddr\":"({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\""""
""""srcPort\":({src_port}\d+)"""
""""dstPort\":({dest_port}\d+)"""
""""protocol\":({protocol}\d+)"""
""""event_type":\"({event_category}[^\"]+)\""""
""""dstScore\":"(0|({alert_severity}[^\"]+))\""""
]
DupFields = [
"alert-severity -> priority"
]
ParserVersion = "v1.0.0"


}
```