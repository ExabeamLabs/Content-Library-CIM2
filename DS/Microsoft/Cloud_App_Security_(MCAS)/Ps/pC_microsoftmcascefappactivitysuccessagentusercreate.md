#### Parser Content
```Java
{
Name = microsoft-mcas-cef-app-activity-success-agentusercreate
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|MCAS|SIEM_Agent|""", """|Create user|""" ]

cef-azure-onedrive-app-activity = {
  Vendor = Microsoft
  Product = Cloud App Security (MCAS)
  TimeFormat = "epoch"
  Fields = [
    """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|""",
    """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|""",
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[^@\s]+)\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)""",
    """\Wc6a1=\s*({src_ip}[A-Fa-f:\d.]+)""",
    """\Wmsg=({additional_info}.*?)\s+(\w+=|$)""",
    """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)""",
    """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)""",
  
}
```