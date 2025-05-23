#### Parser Content
```Java
{
Name = microsoft-mcas-cef-app-activity-success-movemsgtodeletedfolder
  TimeFormat = "epoch"
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|MCAS|SIEM_Agent|""", """|Move messages to Deleted Items folder|""" ]
  Fields = ${MSParsersTemplates.cef-azure-onedrive-app-activity.Fields} [
    """\Wrt=({time}\d{13})""",
  ]

cef-azure-onedrive-app-activity = {
  Vendor = Microsoft
  Product = Microsoft CAS
  TimeFormat = "epoch"
  Fields = [
    """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|""",
    """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|""",
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """destinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=|$)""",
    """\Wc6a1=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\Wmsg=({additional_info}.*?)\s+(\w+=|$)""",
    """\Wmsg=.*?\s+folder\s+(\([^\)]*\):\s*)?({object}.*?)\s+(\w+=|$)""",
    """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=|$)""",
  
}
```