# phoney

`phoney` fetches the frequently released oui.txt by ieee.org and `simplejson.dump`'s the parsed file into a another file a.k.a "The Database".
It also allows you to change the MAC address of an interface.

## Using phoney

Running `phoney` for the first time, it will initially create the Database after downloading the oui.txt

### Listing OUIs by Manufacturer

```bash
phoney search vendor Apple
```

### Search a Manufacturer by OUI/MAC

Argument can be a whitespace separated list of MAC adresses

```bash
phoney search addr 11:22:33:44:55:66 AA:BB:CC:DD:EE:FF
```

### Setting a manufacturer specific MAC address

```bash
phoney set <interface> to vendor Samsung
```

If there is more than one match, `phoney` will ask you to choose from a list of matched manufacturers.

### Setting a specific MAC address

```bash
phoney set <interface> to addr FF:FF:FF:FF:FF:FF
```

### Random pick

```bash
phoney set <interface> to random
```

### Database update

```bash
phoney update
```

# Todo

* `phoney search oui` should accect files



