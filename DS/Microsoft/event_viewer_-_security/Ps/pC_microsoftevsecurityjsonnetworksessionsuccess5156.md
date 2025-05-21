#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-network-session-success-5156
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """"event_id":"5156"""", """"network_information-DestinationAddress"""" ]
  Fields = [
    """({event_name}The Windows Filtering Platform has permitted a connection)""",
    """"host":"({host}[^"]+)"""",
    """"computer":"({host}[^"]+)"""",
    """"event_id":"({event_code}\d+)""",
    """({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (AM|PM|am|pm))""",
    """"message":"({event_name}[^"]+)"""",
    """"network_information-SourceAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?".+?"network_information-Direction":"({direction}Inbound)".+?"network_information-SourcePort":"({=dest_port}\d+)".+?"network_information-DestinationPort":"({src_port}\d+)".+?"computer":"({src_host}[^"]+)".+?"network_information-DestinationAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?"""",
    """"network_information-SourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?".+?"network_information-Direction":"({direction}Outbound)".+?"network_information-SourcePort":"({=src_port}\d+)".+?"network_information-DestinationPort":"({dest_port}\d+)".+?"computer":"({src_host}[^"]+)".+?"network_information-DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=dest_port}\d+))?"""",
    """"network_information-Protocol":"({protocol_id}[^"]+)"""",
    """"application_information-ProcessID":"({process_id}\d+)""",
    """"application_information-ApplicationName":"({process_path}({process_dir}.+)[\\\/]({process_name}.+?))"""",
    """"category":"({category}[^"]+)"""",
    """"filter_information-LayerName":"({layer_name}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```