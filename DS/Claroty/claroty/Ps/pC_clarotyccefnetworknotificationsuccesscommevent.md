#### Parser Content
```Java
{
Name = claroty-c-cef-network-notification-success-commevent
    Vendor = Claroty
    Product = Claroty
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Conditions = ["""CEF:0|Claroty|""","""|comm_event|"""]
    Fields = [
       """\sevent_timestamp=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
       """00\s+({host}[^\s]+)\s+Claroty\s+\d+\s+-""",
       """\s+event_type=({event_name}.+)\s+event_description=""",
       """\ssrc_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """\sdst_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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
       """\sevent_id=({event_code}[^\s]*)""",
       """\|comm_event\|({priority}\d+)\|"""
    ]


}
```