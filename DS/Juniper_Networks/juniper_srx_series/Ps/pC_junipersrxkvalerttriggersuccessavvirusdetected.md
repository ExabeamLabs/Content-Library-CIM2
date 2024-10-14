#### Parser Content
```Java
{
Name = "juniper-srx-kv-alert-trigger-success-avvirusdetected"
Vendor = "Juniper Networks"
Product = "Juniper SRX Series"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""RT_UTM - AV_VIRUS_DETECTED_MT"""
"""name="""
"""filename="""
"""url="""
]
Fields = [
"""\sdestination-address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdestination-port="({dest_port}\d*)"""
"""\s({alert_type}RT_UTM - [^\s]*)\s\["""
"""\s({host}[^\s]*)\sRT_UTM"""
"""\ssource-address="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssource-port="({src_port}\d*)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?"""
"""\susername="(?!N\/A)({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""\ssource-zone-name="({src_network_zone}[^"]*)"""
"""\sfilename="({malware_url}[^"]+)"""
"""\surl="({additional_info}[^"]+)"""
"""\sname="({alert_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```