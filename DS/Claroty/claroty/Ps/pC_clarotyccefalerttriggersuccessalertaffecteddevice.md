#### Parser Content
```Java
{
Name = claroty-c-cef-alert-trigger-success-alertaffecteddevice
    Vendor = Claroty
    Product = Claroty
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Conditions = ["""CEF:0|Claroty|""","""|alert_affected_device|"""]
    Fields = [
       """\s({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
       """\salert_timestamp=({time}[^\s]*)""",
       """00\s+({host}[^\s]+)\s+Claroty\s+\d+\s+-""",
       """\s+alert_name=({alert_name}.+)\s+alert_category=""",
       """\s+alert_type_name=({alert_type_name}.+)\s+alert_name=""",
       """\salert_description=({additional_info}.*?)(?=(?:\s|\||,|;)[\w.-]+=)""",
       """\sdevice_category=({device_category}[^\s]*)""",
       """\sdevice_subcategory=({device_subcategory}[^\s]*)""",
       """\sdevice_asset_id=({device_asset_id}[^\s]*)""",
       """\sdevice_manufacturer=({device_manufacturer}[^\s]*)""",
       """\sdevice_type=({device_type}.*?)(?=(?:\s|\||,|;)[\w.-]+=)""",
       """\sdevice_os=({device_os}.*?)(?=(?:\s|\||,|;)[\w.-]+=)""",
       """\sdevice_site_name=({device_site_name}[^\s]*)""",
       """\sdevice_ip_list=\['({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?[\s',\]]""",
       """\|alert_affected_device\|({alert_severity}\d+)\|""",
       """\s alert_category=({alert_type}[^\s]*)"""
    ]


}
```