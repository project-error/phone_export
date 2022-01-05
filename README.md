# phone_export
 This is an export for the NPWD Phone for ESX to use it as an item

## Configuration

- Config.json
in the config from [NPWD Phone](https://github.com/project-error/npwd/blob/master/config.json) in the lines 1-6 it must look like this to user this Script:

```json
{
  "PhoneAsItem": {
    "enabled": true,
    "exportResource": "phone_export",
    "exportFunction": "canUsePhone"
  },
  ```
- SQL
After this you must excute the SQL in your database to have the item, you must pick your right ESX verion for this:

This is for ESX Version 1.2:

```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES ('phone', 'Smartphone', 1, 0, 1);
```

and this is for ESX Version 1.1:

```sql
INSERT INTO `items` (`name`, `label`, `limit`, `rare`, `can_remove`) VALUES ('phone', 'Smartphone', 1, 0, 1);
```
