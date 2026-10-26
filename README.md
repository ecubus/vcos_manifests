# EcuBus HaloOS / VCOS manifests (PC)

GitHub org forks for native PC / NuttX sim work. Unchanged projects still sync from Gitee `haloos`.

## Init

```bash
repo init -u https://github.com/ecubus/vcos_manifests.git -b frankie/pc -m default.xml
repo sync -j8
```

Or SSH:

```bash
repo init -u git@github.com:ecubus/vcos_manifests.git -b frankie/pc -m default.xml
repo sync -j8
```

## Projects on `ecubus` @ `frankie/pc`

| path | GitHub repo |
| --- | --- |
| `vcos/build` | [ecubus/vcos_build](https://github.com/ecubus/vcos_build) |
| `vcos/vcos_studio` | [ecubus/vcos_studio](https://github.com/ecubus/vcos_studio) |
| `vcos/components/runtime` | [ecubus/vcos_components_runtime](https://github.com/ecubus/vcos_components_runtime) |
| `vcos/components/communication` | [ecubus/vcos_components_communication](https://github.com/ecubus/vcos_components_communication) |
| `vcos/components/rt_framework` | [ecubus/vcos_components_rt_framework](https://github.com/ecubus/vcos_components_rt_framework) |
| `vcos/components/memory` | [ecubus/vcos_components_memory](https://github.com/ecubus/vcos_components_memory) |
| `vcos/apps` | [ecubus/vcos_apps](https://github.com/ecubus/vcos_apps) |
| `vcos/examples` | [ecubus/vcos_examples](https://github.com/ecubus/vcos_examples) |
| `vcos/vendor/ecubus` | [ecubus/EcuBus-Mcal](https://github.com/ecubus/EcuBus-Mcal) |

See `vcos/build/PC_BUILD.md` after sync for the host build command.
