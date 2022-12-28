#### Parser Content
```Java
{
Name = claroty-c-cef-alert-trigger-success-alertaffecteddevice
    Vendor = Claroty
    Product = Claroty
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Conditions = ["""CEF:0|Claroty|Claroty|""","""|alert_affected_device|"""]
    Fields = [
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
       """\sdevice_ip_list=\['({src_ip}[^\s,'\]]*)[\s',\]]""",
       """({src_host}THISWILLNEVERMATCH)""",
       """({user}THISWILLNEVERMATCH)""",
       """\|alert_affected_device\|({alert_severity}\d+)\|""",
       """\s alert_category=({alert_type}[^\s]*)"""
    ]


}
```