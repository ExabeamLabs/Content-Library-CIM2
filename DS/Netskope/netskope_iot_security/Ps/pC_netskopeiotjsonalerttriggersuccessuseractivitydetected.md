#### Parser Content
```Java
{
Name = netskope-iot-json-alert-trigger-success-useractivitydetected
  ParserVersion = v1.0.0
  Conditions = [""""packet_alerts":""", """"category":"User Activity Detected"""", """"signature":"""", """"title":"""" ]

json-netskope-iot-events = {
  Vendor = Netskope
  Product = Netskope IoT Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"source":"({host}[^"]+)"""",
    """"timestamp":"({time}[^"]+)"""",
    """"title":"({alert_name}[^"]+)"""",
    """"signature":"({alert_type}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"id":"({alert_id}[^"]+)"""",
    """"description":"({additional_info}[^"]+)"""",
    """"source":\{[^=]+?"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"source":\{[^=]+?"host_name":"({src_host}[\w.-]+)"""",
    """"source":\{[^=]+?"port":"(:({src_port}\d+))?"""",
    """"source":\{[^=]+?"mac":"({src_mac}[\w.-]+)"""",
    """"source":\{[^=]+?"country":"({src_country}[\w.-]+)"""",
    """"destination":\{[^=]+?"ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"destination":\{[^=]+?"port":"(:({dest_port}\d+))?"""",
    """"destination":\{[^=]+?"mac":"({dest_mac}[\w.-]+)"""",
    """"destination":\{[^=]+?"country":"({dest_country}[\w.-]+)"""",
    """"source":\{[^=]+?"os":"({os}[^"]+)"""",
  
}
```