## SIMP Packer manifests

### Usage
1. Tweak (or generate) the `vars.json` file with appropriate values
2. Validate the setup

  `~/bin/packer validate -var-file=vars.json simp.json`

3. Run packer

   `~/bin/packer build -var-file=vars.json simp.json`

4. Using the default values in `vars.json` a successful build should drop the new VM under `./OUTPUT`.


### TODO
- work on `<wait10>` timings

### DONE
- ~~fix sudo tty issue~~
- ~~put paths, credentials in `-var-` or `-var-file`~~

### packer build --help
```
Usage: packer build [options] TEMPLATE

  Will execute multiple builds in parallel as defined in the template.
  The various artifacts created by the template will be outputted.

Options:

  -debug                     Debug mode enabled for builds
  -force                     Force a build to continue if artifacts exist, deletes existing artifacts
  -machine-readable          Machine-readable output
  -except=foo,bar,baz        Build all builds other than these
  -only=foo,bar,baz          Only build the given builds by name
  -parallel=false            Disable parallelization (on by default)
  -var 'key=value'           Variable for templates, can be used multiple times.
  -var-file=path             JSON file containing user variables.
```
