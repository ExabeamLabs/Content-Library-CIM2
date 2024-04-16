#### Parser Content
```Java
{
Name = wazuh-w-json-peripheral_storage-remove-success-usbdevicedisconnected
  ParserVersion = "v1.0.0"
  Product = Wazuh
  Vendor = Wazuh
  Conditions = [ """"rule.description":"USB device disconnected"""", """"type":"wazuh-alerts"""" ]
  Fields = [
    """exa_regex=agent.labels.agent_hostname":"({src_host}[^"]+)"""",
  ]


}
```