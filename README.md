# sistr --- A Singularity Container


[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/1206)


Singularity container for [sistr](https://github.com/peterk87/sistr_cmd)

## Pre-requisite

Install [Singularity](http://singularity.lbl.gov/docs-installation)

## Usage

### Latest version

The following steps are needed to use the image:

1. Pull the image:

```
singularity pull --name TMP_DIRECTORY shub://phgenomics-singularity/sistr@latest
```
This will command will create a file `sistr.simg`, which is executable.

2. Use the image:
```
./sistr.simg --help
```

### A particular version

```
singularity pull --name mlst shub://phgenomics-singularitysistr@VERSION.NUMBER
```

## Suggested pattern

1. Create a `singularity` folder:

```
mkdir HOME/singularity
```

2. Pull the image to the `singularity` folder.

```
singularity pull --name sistr shub://phgenomics-singularity/sistr@latest
```

3. Link the image to a folder in your `PATH` (e.g., `HOME/bin`)

```
ln -s HOME/singularity/sistr.simg HOME/bin/sistr
```

Now, when you login again, you should be able to just type:

```
sistr --help
```
