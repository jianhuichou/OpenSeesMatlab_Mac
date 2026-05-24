# derived/

This directory is the default location for the compiled OpenSees MATLAB MEX binary.

Place the appropriate pre-compiled MEX file for your platform here before using OpenSeesMatlab:

| Platform | File name |
|---|---|
| macOS Apple Silicon (M-series, `arm64`) | `OpenSeesMATLAB.mexmaca64` |
| macOS Intel (`x86_64`) | `OpenSeesMATLAB.mexmaci64` |
| Windows 64-bit | `OpenSeesMATLAB.mexw64` |

Pre-compiled binaries are provided in the
[releases](https://github.com/jianhuichou/OpenSeesMatlab_Mac/releases) of this repository.

After placing the file here, install the toolbox in MATLAB:

```matlab
installOpenSeesMatlab
```

To verify the MEX file is found, run:

```matlab
opsmat = OpenSeesMatlab();
disp(opsmat.opensees)   % should show status: ready
```

## Building the MEX binary from source

If a pre-compiled binary is not available for your platform, you can build
`OpenSeesMATLAB` from the OpenSees source using MATLAB's `mex` compiler.
Refer to the OpenSees build documentation for details:
<https://opensees.github.io/OpenSeesDocumentation/>
