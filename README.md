# phoney

`phoney` fetches the frequently released oui.txt by ieee.org and stores the OUIs in a local Berkley Hash DB.
It also allows you to change the MAC address of an interface.

## Using phoney

Running `phoney` for the first time, it will initially create the Database after downloading the oui.txt

### Listing OUIs my Manufacturer

```bash
phoney interface -M Apple -l
```

If you run the upper commond without `-l`, the `interface` MAC address will be changed to a random value picked from your `-M` Argument. If there is more than one match, `phoney` will ask you to pick a Manufacturer.

### Search a Manufacturer by OUI/MAC

Argument can be either a list, or a file containing MAC adresses

```bash
phoney interface -o 11:22:33:44:55:66 AA:BB:CC:DD:EE:FF
```

### Random pick

```bash
phoney interface
```

### Setting a specific MAC address

```bash
phoney interface -m FF:FF:FF:FF:FF:FF
```

### Database update

```bash
phoney interface --update-db
```


