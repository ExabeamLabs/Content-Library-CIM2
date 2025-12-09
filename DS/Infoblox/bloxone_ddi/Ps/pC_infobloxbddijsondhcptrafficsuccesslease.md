#### Parser Content
```Java
{
Name = infoblox-bddi-json-dhcp-traffic-success-lease
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"Lease":""", """"LeaseOp":""", """"Code":""", """"GroupName":""", """"Lifetime":""" ]
  Fields = [
    """exa_json_path=$.Lease[0].Cltt,exa_field_name=time""",
    """exa_json_path=$.Group,exa_field_name=group_name""",
    """exa_json_path=$.GroupName,exa_field_name=group_name""",
    """exa_json_path=$.Code,exa_field_name=result""",
    """exa_json_path=$.MsgOp,exa_field_name=status_msg""",
    """exa_json_path=$.Lease[0].LeaseOp,exa_field_name=operation""",
    """exa_json_path=$.Lease[0].Hostname,exa_field_name=src_host""",
    """exa_json_path=$.Lease[0].AddressV0,exa_field_name=src_ip""",
    """exa_json_path=$.Lease[0].AddressV0,exa_field_name=dhcp_ip""",
    """exa_json_path=$.Lease[0].HWAddr,exa_field_name=src_mac""",
    """exa_json_path=$.Lease[0].ClientIDV0,exa_field_name=client_id""",
    """exa_json_path=$.Lease[0].Lifetime,exa_field_name=lease_time""",
    """exa_json_path=$.Lease[0].Type,exa_field_name=dhcp_type"""
  ]
  ParserVersion = v1.0.0


}
```