# Role: check_f5_availability

## Description

This role is part of the F5 BIG-IP platform modernization collection.

## Requirements

- F5 BIG-IP system
- Appropriate network connectivity
- Valid credentials

## Role Variables

See defaults/main.yml for available variables (if present).

## Dependencies

None

## Example Usage

```yaml
- hosts: f5_devices
  roles:
    - f5devcentral.f5_bd_ansible_platform_modernization.check_f5_availability
```

## License

GPL-3.0-or-later

## Author

F5 DevCentral
