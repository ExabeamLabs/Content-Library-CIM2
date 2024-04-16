#### Parser Content
```Java
{
Name = microsoft-mdhcplog-json-endpoint-notification-success-dhcpadminevents
 Conditions = [""""LogName":"DhcpAdminEvents"""", """"ProviderName":"Microsoft-Windows-DHCP-Server"""", """"MachineName":""", """"Properties":""", """"Message":"""]
 ParserVersion = v1.0.0

json-microsoft-windows-dhcp-events = {
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  TimeFormat = "epoch"
  Fields = [
   """"TimeCreated":"\\\/Date\(({time}\d{13})""",
   """"MachineName":"({host}[\w.-]+)"""",
   """"LogName":"({event_name}[^"]+)"""",
   """UserId[^=]+?Value":"({user_sid}[^"]+)[^:]+?,"TimeCreated""""
   """"Message":"({additional_info}[^"]+)"""",
  
}
```