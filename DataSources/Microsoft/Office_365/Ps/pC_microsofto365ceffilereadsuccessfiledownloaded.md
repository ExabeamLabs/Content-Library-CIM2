#### Parser Content
```Java
{
Name = microsoft-o365-cef-file-read-success-filedownloaded
  Conditions = [ """|Microsoft|""", """|FileDownloaded|""", """eventId=""" ]
  ParserVersion = v1.0.0

cef-o365-file-read = {
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wact=({access}.+?)\s*(\w+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)\s*(\w+=|$)""",
    """\Wsrc=({src_ip}[a-fA-F:\d.]+)""",
    """\Wcs5=({app}.+?)\s*(\w+=|$)""",
    """\Wdvc=({host}\S+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wduser=({email_address}[^@\s]+@[^\s@]+)""",
    """\Wsuser=({email_address}[^@\s]+@[^\s@]+)""",
    """\Wsuid=(?!\S+@\S+)({user}[^\s]+)\s*(\w+=|$)""",
    """\Wsuid=({email_address}[^\s@]+@[^\s]+)\s*(\w+=|$)""",
    """\WfilePath=({src_file_path}.+?)\s*(\w+=|$)""",
    """\WfilePath=(({file_dir}.+?)\/({file_name}[^\/]+?))\s*(\w+=|$)""",
    """\WfilePath=.*?(\.({src_file_ext}[^\/\.]*?))?\s*(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s*(\w+=|$)""",
    """\WrequestClientApplication=({user_agent}.+?)\s*(\w+=|$)""",
  
}
```