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

## Inputs

| Name          | Description                       | Required | Default |
|---------------|-----------------------------------|----------|---------|
| `pdk_name`    | The name of the PDK to install    | No       | sky130  |
| `pdk_version` | The version of the PDK to install | Yes      |         |
| `pdk_root`    | Where to install to PDK           | No       | ~/.ciel |

## Updating the action

To update the release tag of the action, run the following commands:

```bash
git tag -fa v1 -m "Update action"
git push origin v1 --force
```

## License

[Apache 2.0](LICENSE)
