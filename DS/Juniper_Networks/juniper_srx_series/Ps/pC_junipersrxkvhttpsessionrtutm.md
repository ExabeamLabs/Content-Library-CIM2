#### Parser Content
```Java
{
Name = "juniper-srx-kv-http-session-rtutm"
Vendor = "Juniper Networks"
Product = "Juniper SRX Series"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""RT_UTM - WEBFILTER_URL_"""
""" url=""""
""" category=""""
]
Fields = [
"""\sdestination-address="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdestination-port="({dest_port}\d*)"""
"""\s({host}[^\s]*)\sRT_UTM"""
"""\ssource-address="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssource-port="({src_port}\d*)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(?:z|Z)?"""
"""\susername="(?!N\/A)({user}[^"]+)""""
"""\ssource-zone-name="({src_network_zone}[^"]*)"""
"""\sprofile="({profile}[^"]+)"""
"""\sname="({alert_name}[^"]+)"""
"""\scategory="({category}[^"]+)"""
"""({action}PERMITTED|BLOCKED)"""
"""\sreason="({failure_reason}[^"]+)"""
"""\surl="({web_domain}[^"]+)"""
"""\sobj="({uri_path}\/[^\s\?]+)?({uri_query}\?[^\s]+)?""""
]
ParserVersion = "v1.0.0"


}
```