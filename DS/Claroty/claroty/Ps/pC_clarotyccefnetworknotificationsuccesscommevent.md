#### Parser Content
```Java
{
Name = claroty-c-cef-network-notification-success-commevent
    Vendor = Claroty
    Product = Claroty
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Conditions = ["""CEF:0|Claroty|Claroty|""","""|comm_event|"""]
    Fields = [
       """\sevent_timestamp=({time}[^\s]*)""",
       """00\s+({host}[^\s]+)\s+Claroty\s+\d+\s+-""",
       """\s+event_type=({event_name}.+)\s+event_description=""",
       """\ssrc_ip=({src_ip}[^\s]*)""",
       """\sdst_ip=({dest_ip}[^\s]*)""",
       """\sevent_description=({additional_info}.*?)(?=(?:\s|\||,|;)[\w.-]+=)""",
       """\sdevice_category=({device_category}[^\s]*)""",
       """\sdevice_subcategory=({device_subcategory}[^\s]*)""",
       """\sdevice_asset_id=({device_asset_id}[^\s]*)""",
       """\sdevice_manufacturer=({device_manufacturer}[^\s]*)""",
       """\sdevice_type=({device_type}.*?)(?=(?:\s|\||,|;)[\w.-]+=)""",
       """\sdevice_os=({device_os}.*?)(?=(?:\s|\||,|;)[\w.-]+=)""",
       """\ssrc_port=({src_port}\d+)""",
       """\sdst_port=({dest_port}\d+)""",
       """\sdevice_site_name=({device_site_name}[^\s]*)""",
       """\sprotocol=({protocol}[^\s]*)""",
       # """({bytes}THISWILLNEVERMATCH)""",
       """\sevent_id=({event_code}[^\s]*)""",
       """\|comm_event\|({priority}\d+)\|""",
       # """({packets}THISWILLNEVERMATCH)""",
       """({direction}THISWILLNEVERMATCH)"""
    ]


}
```