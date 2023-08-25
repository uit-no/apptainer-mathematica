# Local Mathematica via Apptainer/Singularity

## Prerequisites

- Apptainer or Singularity
- A valid Mathematica license file

## Installation

### Step 1: Download the container image

First, pull the image from the release page:
```
$ singularity pull https://github.com/uit-no/apptainer-mathematica/releases/download/0.0.1/mathematica.sif
```
or
```
$ apptainer pull https://github.com/uit-no/apptainer-mathematica/releases/download/0.0.1/mathematica.sif
````

### Step 2: Locate your Mathematica license file
Ensure you have a valid Mathematica license file accessible on your local machine. This is required to run the container.



## Usage

### Running a Mathematica Script (.wl)

To run your Mathematica script, use the following command with singularity:

```
$ singularity run --bind path_to_license_file:/root/.WolframEngine/Licensing/mathpass mathematica.sif your_script.wl
```

or with Apptainer

```
$ apptainer run --bind path_to_license_file:/root/.WolframEngine/Licensing/mathpass mathematica.sif your_script.wl
```
