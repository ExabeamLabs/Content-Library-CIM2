#### Parser Content
```Java
{
Name = swipes-s-kv-physical-location-access-success-swipes
    Vendor = Swipes
    Product = Swipes
    ParserVersion = v1.0.0
    TimeFormat = "yyyy/MM/dd HH:mm:ss.SSS"
    Conditions = [ """_index=swipes""" ]
    Fields = [
      """_host=(.+?@\s*)?({host}[^\s]+)""",
      """_raw=([^\|]*\|){4}({time}[^\|]+)\|""",
      """_raw=({department}[^\|]+)\|""",
      """_raw=([^\|]*\|)({last_name}[^\|]+)\|""",
      """_raw=([^\|]*\|){2}({first_name}[^\|]+)\|""",
      """_raw=([^\|]*\|){5}({location_area}[^\|]+)\|""",
      """_raw=([^\|]*\|){6}({location_door}[^\|]+)\|""",
      """_raw=([^\|]*\|){7}({badge_id}[^\|]+)\|""",
    ]
    DupFields = ["location_area->location_building"]


}
```