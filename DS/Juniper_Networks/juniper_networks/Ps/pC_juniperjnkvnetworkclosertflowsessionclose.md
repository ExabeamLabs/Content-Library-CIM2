#### Parser Content
```Java
{
Name = juniper-jn-kv-network-close-rtflowsessionclose
    Vendor = Juniper Networks
    Product = Juniper Networks
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """RT_FLOW_SESSION_CLOSE""", """encrypted=""" ]
    Fields = [
       """encrypted="({additional_info}[^"]+)""",
        """destination-address="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """destination-port="({dest_port}\d+)""",
        """RT_FLOW\s-\s({event_name}[^\s]+)\s\[""",
        """\s({host}[^\s]+)\sRT_FLOW""",
        """packet-incoming-interface="({src_interface}[^"]+)""",
        """source-address="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """source-port="({src_port}\d+)""",
        """\s\d+\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).\d\d\dZ\s\S+\sRT_FLOW""",
        """username="(?!N\/A)({user}[^"]+)"""",
        """protocol-id="({protocol}[^"]+)""",
        """destination-zone-name="({dest_network_zone}[^"]+)""",
        """reason="({miscellaneous}[^"]+)""",
        """\sapplication="({network_app}[^"]+)""",
        """policy-name="({policy_name}[^"]+)""",
        """source-zone-name="({src_network_zone}[^"]+)""",
        """nested-application="({subtype}[^"]+)""",
        """service-name="({service_name}[^"]+)"""
    ]
        ParserVersion = "v1.0.0"


}
```