#### Parser Content
```Java
{
Name = microsoft-o365-cef-file-read-success-pageviewed
  Conditions = [ """|Microsoft|""", """|PageViewed|""", """eventId=""" ]
  ParserVersion = v1.0.0

cef-o365-file-read = {
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wact=({access}.+?)\s*(\w+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)\s*(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wcs5=({app}.+?)\s*(\w+=|$)""",
    """\Wdvc=({host}\S+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wduser=({email_address}[^@\s]+@[^\s@]+)""",
    """\Wsuser=({email_address}[^@\s]+@[^\s@]+)""",
    """\Wsuid=(?!\S+@\S+)({user}[^\s]+)\s*(\w+=|$)""",
    """\Wsuid=({email_address}[^\s@]+@[^\s]+)\s*(\w+=|$)""",
    """\WfilePath=({file_path}.+?)\s*(\w+=|$)""",
    """\WfilePath=(({file_dir}.+?)\/({file_name}[^\/]+?))\s*(\w+=|$)""",
    """\WfilePath=.*?(\.({file_ext}[^\/\.]*?))?\s*(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s*(\w+=|$)""",
    """\WrequestClientApplication=({user_agent}.+?)\s*(\w+=|$)""",
  
}
```