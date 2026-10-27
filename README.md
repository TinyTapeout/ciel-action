# ciel-action

GitHub action for installing open source PDKs using [ciel](https://pypi.org/project/ciel/).

## Usage

Add the following step to your workflow:

```yaml
- name: Install Sky130 PDK
  uses: TinyTapeout/ciel-action@v1
  with:
    pdk_name: sky130
    pdk_version: 12df12e2e74145e31c5a13de02f9a1e176b56e67
    pdk_root: /home/runner/pdk
```

IHP PDKs use the variant name, e.g. `ihp-sg13g2` or `ihp-sg13cmos5l`:

```yaml
- name: Install IHP SG13CMOS5L PDK
  uses: TinyTapeout/ciel-action@v1
  with:
    pdk_name: ihp-sg13cmos5l
    pdk_version: 89d42ee6d2fd9b50b86a1aada6fee6673c3e6008
    pdk_root: /home/runner/pdk
```

## Inputs

| Name          | Description                       | Required | Default |
|---------------|-----------------------------------|----------|---------|
| `pdk_name`    | The name of the PDK to install    | No       | sky130  |
| `pdk_version` | The version of the PDK to install | Yes      |         |
| `pdk_root`    | Where to install to PDK           | No       | ~/.ciel |
| `ciel_version`| The version of ciel to use        | No       | 3.2.0   |

## Updating the action

To update the release tag of the action, run the following commands:

```bash
git tag -fa v1 -m "Update action"
git push origin v1 --force
```

## License

[Apache 2.0](LICENSE)
